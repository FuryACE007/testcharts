<template>
  <div id="chart">
    <apex-chart
      height="350"
      type="area"
      :options="chartOptions"
      :series="series"
    >
    </apex-chart>
  </div>
</template>

<script>
export default {
  name: "BP",
  data: () => ({
    series: [
      {
        name: "Pre BP Stolic", //name of the graph
        data: dates,
      },
      //   {
      //     name: "Post BP Stolic",
      //     data: dates,
      //   },
    ],
    chartOptions: {
      chart: {
        type: "area",
        stacked: false,
        height: 350,
        zoom: {
          type: "x",
          enabled: true,
          autoScaleYaxis: true, // scales the y axis automatically based on the data
        },
        toolbar: {
          autoSelected: "zoom",
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
      dropShadow: {
        enabled: true,
        top: -2,
        left: 2,
        blur: 5,
        opacity: 0.18,
      },
      title: {
        text: "Pre & Post BP Stolic/Diastolic",
      },
      legend: {
        position: "top",
        horizontalAlign: "center",
      },
      yaxis: {
        title: {
          text: "BP Stolic/Diastolic of patient",
        },
        tooltip: {
          enabled: true
        },
      },
      xaxis: {
        title: {
          text: "Date",
        },
        type: "datetime",
        axisBorder: {
          show: false
        },
        axisTicks: {
          show: false
        },
      },
      colors:['#A2D5AB'],
      fill: {
        type: "solid",
        fillOpacity: 0.7
      },
      grid: {
        padding: {
          left: -5,
          right: 5
        }
      },
      tooltip: {
        x: {
          format: "dd MMM yyyy"
        },
      },
    },
  }),
};
</script>

<style></style>
