<template>
  <div class="background">
    <img src="https://i.postimg.cc/HsRxZVD9/background-1.png">
  </div>
  <div class="container">
    <table class="crypto-coin">
      <thead>
        <tr>
          <th @onclick="sortTable('Rank')">Rank</th>
          <th @onclick="sortTable('CoinName')">CoinName</th>
          <th @onclick="sortTable('CoinSymbol')">CoinSymbol</th>
          <th @onclick="sortTable('Price')">Price</th>
          <th @onclick="sortTable('price_change_percentage_1h_in_currency')">1h</th>
          <th @onclick="sortTable('Market Cap')">Market Cap</th>
        </tr>
      </thead>
      <tbody id="body">
        <tr v-for="crypto in sortedCrypto" :key="crypto.id">
            <td class="rank">{{ crypto.rank }}</td>
            <td>
              <img :src="crypto.image" :alt="crypto.name" class="coin-icon" />
              {{ crypto.name }}
            </td>
            <td>{{ crypto.symbol }}</td>
            <td>{{ 'ZAR ' + crypto.current_price.toFixed(2) }}</td>
            <td>{{ crypto.price_change_percentage_1h_in_currency }}</td>
            <td>{{ 'ZAR ' + crypto.market_cap.toLocaleString() }}</td>
          </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import axios from 'axios';
import { computed } from 'vue';
export default {
  data() {
      return {
        cryptoData: [],
        sortKey: '',
        sortTable: 1,
      };
    },
    computed: {
      sortedCrypto() {
        const sorted = this.cryptoData.slice().sort((a, b) => {
          const keyA = a[this.sortKey];
          const keyB = b[this.sortKey];
          return this.sortTable * (keyA > keyB ? 1 : -1);
        });
        return sorted;
      },
    },
    methods: {
      async fetchData() {
        try {
          const response = await axios.get(
            'https://api.coingecko.com/api/v3/coins/markets',
            {
              params: {
                vs_currency: 'zar',
                ids: 'bitcoin,ethereum,ripple,cardano,polkadot,binancecoin,dogecoin,litecoin,uniswap,avalanche-2',
                order: 'market_cap_desc',
                per_page: 10,
                page: 1,
                sparkline: false,
                localization: false,
              },
            }
          );
          this.cryptoData = response.data;
          const coinIds = this.cryptoData.map((crypto) => crypto.id).join(',');
          const metadataResponse = await axios.get(
            `https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&ids=${coinIds}`
          );
          const metadataMap = new Map(metadataResponse.data.map((crypto) => [crypto.id, crypto]));
          this.cryptoData.forEach((crypto, index) => {
            if (metadataMap.has(crypto.id)) {
              crypto.image = metadataMap.get(crypto.id).image;
              crypto.rank = index + 1;
            }
          });
        } catch (error) {
          console.error('Error fetching data:', error);
        }
      },
      sort(key) {
        if (this.sortKey === key) {
          this.sortTable *= -1;
        } else {
          this.sortKey = key;
          this.sortTable = 1;
        }
      },
    },
    mounted() {
      this.fetchData();
    },
    
}
</script>
<style scoped>
.container {
  position:absolute;
  max-width: 100px;
  top: 50%;
  left: 30%;
  transform: translate(-50%, -50%);
}
.crypto-coin{
  max-width: 100px;
  border-collapse: collapse;
  border: 1px solid #000000;
}
.crypto-coin th{
  font-size: 18px;
  white-space: nowrap;
  padding: 18px 12px;
} 
  .coin-icon {
    width: 20px;
    height: 20px;
    margin-right: 10px;
    inline-size: 20px;
  }
  .rank {
    font-weight: bold;
  }
.background img{
  /* width: 100vw;
  height: 100vh; */
}
</style>
