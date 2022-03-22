<template>
  <div id="chart">
    <apex-chart
      height="450"
      width="750"
      type="line"
      :options="chartOptions"
      :series="series"
    >
    </apex-chart>
  </div>
</template>

<script>
export default {
  name: "Creatinine-chart",
  data: () => ({
    series: [
      {
        name: "Creatinine", //name of the graph
        data: [
          { x: "04/13/2021", y: 4 },
          { x: "04/14/2021", y: 4 },
          { x: "04/15/2021", y: 4 },
          { x: "04/16/2021", y: 4 },
          { x: "04/17/2021", y: 4 },
          { x: "04/18/2021", y: 4 },
          { x: "04/19/2021", y: 3 },
          { x: "04/20/2021", y: 4 },
          { x: "04/21/2021", y: 3 },
          { x: "04/22/2021", y: 3 },
          { x: "04/23/2021", y: 3 },
          { x: "04/24/2021", y: 3 },
          { x: "04/25/2021", y: 4 },
          { x: "04/26/2021", y: 4 },
          { x: "04/27/2021", y: 4 },
          { x: "04/28/2021", y: 3 },
          { x: "04/29/2021", y: 3 },
          { x: "04/30/2021", y: 3 },
          { x: "04/31/2021", y: 3 },
          // 5,6,7
        ],
      },
      //   {
      //     name: "Post BP Stolic",
      //     data: dates,
      //   },
    ],
    chartOptions: {
      chart: {
        type: "line",
        stacked: false,
        height: 350,
        width: "100%",
        zoom: {
          type: "x",
          enabled: true,
          autoScaleYaxis: true, // scales the y axis automatically based on the data
        },
        toolbar: {
          autoSelected: "zoom",
        },
        animations: {
          enabled: true,
          easing: "easeinout",
          speed: 800,
          animateGradually: {
            enabled: true,
            delay: 150,
          },
        },
        dropShadow: {
          enabled: true,
          top: -2,
          left: 2,
          blur: 5,
          opacity: 0.18,
        },
      },
      dataLabels: {
        enabled: false,
      },
      stroke: {
        curve: "smooth",
        width: 3,
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

      title: {
        text: "Creatinine Value",
        align: "center",
      },
      legend: {
        show: true,
        showForSingleSeries: true,
        position: "bottom",
        horizontalAlign: "center",
        onItemClick: {
          toggleDataSeries: true,
        },
        onItemHover: {
          highlightDataSeries: true,
        },
      },
      yaxis: {
        title: {
          text: "Creatinine",
          style: {
            fontSize: "13px",
          },
        },
        min: 3,
        max: 7,
        tooltip: {
          enabled: true,
        },
      },
      xaxis: {
        title: {
          text: "Date",
        },
        type: "datetime",
        axisBorder: {
          show: false,
        },
        axisTicks: {
          show: false,
        },
      },
      colors: ["#A2D5AB"],
      fill: {
        type: "solid",
        fillOpacity: 0.7,
      },
      // grid: {
      //   padding: {
      //     left: -5,
      //     right: 5,
      //   },
      // },
      tooltip: {
        x: {
          format: "dd MMM yyyy",
        },
      },
    },
  }),
};
</script>

<style></style>
