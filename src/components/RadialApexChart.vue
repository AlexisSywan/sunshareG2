<template>
    <vue-apex-charts type=radialBar height=350 :options="chartOptions" :series="series"/>
</template>

<script>
    import VueApexCharts from 'vue-apexcharts'

    export default {
        name: "RadialApexChart",
        components: {
            VueApexCharts
        },
        data() {
            return {
                series: [76, 67],
                chartOptions: {
                    plotOptions: {
                        radialBar: {
                            offsetY: -10,
                            startAngle: 0,
                            endAngle: 270,
                            hollow: {
                                margin: 5,
                                size: '30%',
                                background: 'transparent',
                                image: undefined,
                            },
                            dataLabels: {
                                name: {
                                    show: false,

                                },
                                value: {
                                    show: false,
                                }
                            }
                        }
                    },
                    colors: ['#1ab7ea', '#ffa000'],
                    labels: ['Production', 'Consommation'],
                    legend: {
                        show: true,
                        floating: true,
                        fontSize: '16px',
                        position: 'left',
                        offsetX: 160,
                        offsetY: 10,
                        labels: {
                            useSeriesColors: true,
                        },
                        markers: {
                            size: 0
                        },
                        formatter: function (seriesName, opts) {
                            return seriesName + ":  " + opts.w.globals.series[opts.seriesIndex]
                        },
                        itemMargin: {
                            horizontal: 1,
                        }
                    },
                    responsive: [{
                        breakpoint: 480,
                        options: {
                            legend: {
                                show: false
                            }
                        }
                    }]
                }
            }
        }
    }
</script>

<style scoped>

</style>
