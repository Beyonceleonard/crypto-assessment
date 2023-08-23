<template>
  <div class="container">
    <table class="crypto-coin">
      <thead>
        <tr>
          <th onclick="sortTable(0)">Rank</th>
          <th onclick="sortTable(1)">CoinSymbol</th>
          <th onclick="sortTable(2)">CoinName</th>
          <th onclick="sortTable(3)">Price</th>
          <th onclick="sortTable(4)">1h</th>
          <th onclick="sortTable(5)">Market Cap</th>
        </tr>
      </thead>
      <tbody id="body"></tbody>
    </table>
  </div>
</template>

<script>
import axios from 'axios';
import { computed } from 'vue';
export default {
 data() {
  return{
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
  }

 }
}
</script>
<style scoped>
.container {
  position:absolute;
  width: 600px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.table{
  min-width: 100%;
  table-layout: fixed;
  border-collapse: collapse;
  border: 1px solid #81adb7;
}
.table th{
  font-size: 12px;
  white-space: nowrap;
  padding: 8px 12px;
}

</style>
