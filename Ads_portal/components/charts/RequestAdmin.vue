<template>
    <div class="chart">
      <div class="header  flex flex-row items-center justify-between">
        <div class="title">
          <span>Track ad request</span>
        </div>
        <div class="input-date">
          <span>Total: {{ userTotal }}</span>
        </div>
      </div>
      <canvas id="TrackRequestAdmin" class="h-full"></canvas>
    </div>
  </template>
  
  <script setup lang="ts">
  import { Chart } from "chart.js/auto";
  import { onMounted, ref } from "vue";
//   import { format } from "date-fns";
  const userTotal = ref();
  const counts: number[] = [100,26,40,43];
  const times: string[] = ["23","343","32","43"];
  
  const data = {
    labels: times,
    datasets: [
      {
        label: "Active users",
        backgroundColor: "white",
        data: counts,
        tension: 0.3,
        borderColor: 'teal',
        pointBorderWidth: 2,
        pointBackgroundColor:'teal',
        pointBorderColor:'white'
      },
    ],
  };
  
  const config: any = {
    type: "line",
    data: data,
    options: {
      ticks: {
        stepSize: 1
      }
    },
  };
  onMounted(async () => {
    // await getDAU();
    const canvasElement = document.getElementById(
      "TrackRequestAdmin"
    ) as HTMLCanvasElement | null;
    if (canvasElement) {
      new Chart(canvasElement, config);
    }
  });
  
  //================= DAU admin page ==============//
//   const getDAU = async () => {
//     const response = await callAPI("/api/analytics/admin/getDAU");
//     const adminDAU = response.data.user_counts;
//     userTotal.value = response.data.total_users;
//     for (let i = 0; i < adminDAU.length; i++) {
//       counts.push(adminDAU[i].user_count);
//       const dateTime = format(new Date(adminDAU[i].time), 'p')
//       times.push(dateTime);
//     }
//   };
  </script>
  <style scoped>
  span {
    color:#F4CE14;
  }
  .chart {
    
    background: #2A2D3E;
    border-radius:10px;
    @apply  shadow-sm p-3 sm:p-5;
  }
  
  .title {
    color: gray;
  }
  
  .header {
    padding: 5px;
  }
  
  .input-date {
    display: flex;
    flex-direction: row;
    gap: 10px;
    color: var(--primary-color);
  }
  
  .input-date input {
    padding: 7px;
    width: 200px;
    background: #74c0fc;
    color: #ffff;
  }
  </style>
  