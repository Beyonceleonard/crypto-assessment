<template>
  <div class="background">
     <img src="https://i.postimg.cc/HsRxZVD9/background-1.png" style="width: 100vw; height: 100vh; background-size: cover; margin-top: 70px;">
  </div>
  <div class="container">
    <table class="coin-prices">
      <thead>
        <tr>
          <th>Rank</th>
          <th @onclick="sort('coinName')">Coin Name</th>
          <th @onclick="sort('symbol')">Coin Symbol</th>
          <th @onclick="sort('price')">Price</th>
          <th @onclick="sort('price_change_percentage')">1h Move</th>
          <th @onclick="sort('market_cap')">Market Cap</th>
        </tr>
      </thead>
      <tbody id="body">
        <tr v-for="crypto in sortedCrypto" :key="crypto.id">
          <td class="rank">{{ crypto.rank }}</td>
            <td><img :src="crypto.image" alt="crypto.name" class="crypto-coin">{{ crypto.name }}</td>
            <td>{{ crypto.symbol }}</td>
            <td>{{ 'ZAR ' + crypto.current_price.toFixed(2) }}</td>
            <td>{{ crypto.price_change_percentage }}</td>
            <td>{{ 'ZAR ' + crypto.market_cap.toLocaleString() }}</td>
          </tr>
      </tbody>
    </table>
    <router-link class="contact" to="/contact">Next</router-link>
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
        sortOrder: 1,
      };
    },
    computed: {
      sortedCrypto() {
        const sorted = this.cryptoData.slice().sort((a, b) => {
          const keyA = a[this.sortKey];
          const keyB = b[this.sortKey];
          return this.sortOrder * (keyA > keyB ? 1 : -1);
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
          this.sortOrder *= -1;
        } else {
          this.sortKey = key;
          this.sortOrder = 1;
        }
      },
    },
    mounted() {
      this.fetchData();
    },
  };
</script>
<style scoped>
.container {
  position:absolute;
  max-width: 100px;
  top: 60%;
  left: 30%;
  transform: translate(-50%, -50%);
}
.coin-prices{
  max-width: 100px;
  border-collapse: collapse;
  border: 1px solid #000000;
}
.coin-prices th{
  font-size: 18px;
  white-space: nowrap;
  padding: 18px 12px;
} 
.crypto-coin {
    width: 20px;
    height: 20px;
    margin-right: 10px;
  }

</style>
