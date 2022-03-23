<template>
  <div id="wrapper">
    <div id="chart-line2">
      <apex-chart
        type="line"
        height="350"
        width="800"
        :options="chartOptions"
        :series="series"
      ></apex-chart>
    </div>
    <div id="chart-line">
      <apex-chart
        type="area"
        height="130"
        width="800"
        :options="chartOptionsLine"
        :series="seriesLine"
      ></apex-chart>
    </div>
  </div>
</template>

<script>
export default {
  name: "Weight-chart",
  data: () => ({
    //Line Chart
    series: [
      {
        name: "Pre-dialysis Weight",
        data: [
          { x: "04/13/2021", y: 70 },
          { x: "04/14/2021", y: 67 },
          { x: "04/15/2021", y: 71 },
          { x: "04/16/2021", y: 67 },
          { x: "04/17/2021", y: 69 },
          { x: "04/18/2021", y: 70 },
          { x: "04/19/2021", y: 72 },
          { x: "04/20/2021", y: 69 },
          { x: "04/21/2021", y: 71 },
          { x: "04/22/2021", y: 68 },
          { x: "04/23/2021", y: 69 },
          { x: "04/24/2021", y: 73 },
          { x: "04/25/2021", y: 70 },
          { x: "04/26/2021", y: 69 },
          { x: "04/27/2021", y: 67 },
          { x: "04/28/2021", y: 72 },
          { x: "04/29/2021", y: 70 },
          { x: "04/30/2021", y: 73 },
          { x: "04/31/2021", y: 72 },
        ],
      },
      {
        name: "Post-dialysis Weight",
        data: [
          { x: "04/13/2021", y: 67 },
          { x: "04/14/2021", y: 65 },
          { x: "04/15/2021", y: 70 },
          { x: "04/16/2021", y: 65 },
          { x: "04/17/2021", y: 67 },
          { x: "04/18/2021", y: 69 },
          { x: "04/19/2021", y: 70 },
          { x: "04/20/2021", y: 69 },
          { x: "04/21/2021", y: 70 },
          { x: "04/22/2021", y: 67 },
          { x: "04/23/2021", y: 65 },
          { x: "04/24/2021", y: 70 },
          { x: "04/25/2021", y: 70 },
          { x: "04/26/2021", y: 67 },
          { x: "04/27/2021", y: 67 },
          { x: "04/28/2021", y: 70 },
          { x: "04/29/2021", y: 67 },
          { x: "04/30/2021", y: 70 },
          { x: "04/31/2021", y: 70 },
        ],
      },
    ],
    chartOptions: {
      chart: {
        id: "chart2",
        type: "line",
        height: 230,
        toolbar: {
          autoSelected: "pan",
          show: false,
        },
        dropShadow: {
          enabled: true,
          top: -2,
          left: 2,
          blur: 5,
          opacity: 0.18,
        },
      },
      colors: ["#FFB2A6","#9ADCFF"],
      stroke: {
        width: 3,
        curve: "smooth",
      },
      dataLabels: {
        enabled: false,
      },
      legend: {
        show: true,
        showForSingleSeries: true,
        position: "top",
        horizontalAlign: "center",
        onItemClick: {
          toggleDataSeries: true,
        },
        onItemHover: {
          highlightDataSeries: true,
        },
      },
      title: {
        text: "Weight",
        align: "left",
        style: {
          fontSize: "20px",
        },
      },
      fill: {
        opacity: 1,
      },
      markers: {
        size: 4,
        strokeColor: "#F8EDE3",
        strokeWidth: 3,
        strokeOpacity: 1,
        fillOpacity: 1,
        hover: {
          size: 6,
        },
      },
      xaxis: {
        type: "datetime",
      },
      yaxis:{
          title:{
                text: "Weight (kg)"
          }
      }
    },
    //Area Chart
    seriesLine: [
      {
        data: [
          { x: "04/13/2021", y: 70 },
          { x: "04/14/2021", y: 67 },
          { x: "04/15/2021", y: 71 },
          { x: "04/16/2021", y: 67 },
          { x: "04/17/2021", y: 69 },
          { x: "04/18/2021", y: 70 },
          { x: "04/19/2021", y: 72 },
          { x: "04/20/2021", y: 69 },
          { x: "04/21/2021", y: 71 },
          { x: "04/22/2021", y: 68 },
          { x: "04/23/2021", y: 69 },
          { x: "04/24/2021", y: 73 },
          { x: "04/25/2021", y: 70 },
          { x: "04/26/2021", y: 69 },
          { x: "04/27/2021", y: 67 },
          { x: "04/28/2021", y: 72 },
          { x: "04/29/2021", y: 70 },
          { x: "04/30/2021", y: 73 },
          { x: "04/31/2021", y: 72 },
        ],
      },
    ],
    chartOptionsLine: {
      chart: {
        id: "chart1",
        height: 130,
        type: "area",
        brush: {
          target: "chart2",
          enabled: true,
        },
        selection: {
          enabled: true,
          xaxis: {
            min: new Date("19 Jan 2021").getTime(),
            max: new Date("14 May 2021").getTime(),
          },
        },
      },
      colors: ["#008FFB"],
      fill: {
        type: "gradient",
        gradient: {
          opacityFrom: 0.91,
          opacityTo: 0.1,
        },
      },
      xaxis: {
        type: "datetime",
        tooltip: {
          enabled: false,
        },
      },
      yaxis: {
        tickAmount: 2,
        min: 55,
        max: 90,
      },
    },
  }),
};
</script>

<style></style>
