<template>
  <div class="background">
    <img src="https://i.postimg.cc/HsRxZVD9/background-1.png" style="width: 100vw; height: 100vh; background-size: cover;">
  </div>
  <div class="container">
    <table class="spot-prices">
      <thead>
        <tr>
          <th @onclick="sortTable('FullName')">FullName</th>
          <th @onclick="sortTable('Price')">Price</th>
          <th @onclick="sortTable('Move')">Move</th>
          <th @onclick="sortTable('Percentage Move')">PercentageMove</th>
          <th @onclick="sortTable('Time')">Time</th>
        </tr>
      </thead>
      <tbody id="body">
        <tr v-for="spot in sortedSpotData" :key="spot.id">
            <td>{{ spot.FullName }}</td>
            <td>{{ 'ZAR ' + Price.toFixed(2) }}</td>
            <td>{{ spot.Move }}</td>
            <td>{{ 'ZAR ' + spot.PercentageMove.toLocaleString() }}</td>
            <td>{{ spot.Time }}</td>
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
        spotData: [],
        sortKey: '',
        sortTable: 1,
      };
    },
    computed: {
      sortedSpotData() {
        const sorted = this.spotData.slice().sort((a, b) => {
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
            'https://api.sharenet.co.za/api/v1/px2/spots',
          );
          this.spotData = response.data;
          const spotIds = this.spotData.map((spot) => spot.id).join(',');
          const metadataResponse = await axios.get(
            `https://api.sharenet.co.za/api/v1/px2/spots=${spotIds}`
          );
          const metadataMap = new Map(metadataResponse.data.map((spot) => [spot.id, spot]));
          this.spotData.forEach((spot, index) => {
            if (metadataMap.has(spot.id)) {
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
.spot-prices{
  max-width: 100px;
  border-collapse: collapse;
  border: 1px solid #000000;
}
.spot-prices th{
  font-size: 18px;
  white-space: nowrap;
  padding: 18px 12px;
} 

</style>
