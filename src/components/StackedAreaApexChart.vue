<template>
    <vue-apex-charts type=area height=350 max-width=100% :options="chartOptions" :series="series"/>
</template>

<script>
    import VueApexCharts from 'vue-apexcharts'

    export default {
        name: "StackedAreaApexChart",
        components: {
            VueApexCharts
        },
        data() {
            return {
                series: [
                    {
                        name: 'Soutir',
                        data: this.generateDayWiseTimeSeries(new Date('11 Feb 2017 GMT').getTime(), 20, {
                            min: -10,
                            max: 60
                        })
                    },
                    {
                        name: 'Inject',
                        data: this.generateDayWiseTimeSeries(new Date('11 Feb 2017 GMT').getTime(), 20, {
                            min: -10,
                            max: 20
                        })
                    },
                    {
                        name: 'Autoconsommation',
                        data: this.generateDayWiseTimeSeries(new Date('11 Feb 2017 GMT').getTime(), 20, {
                            min: -10,
                            max: 15
                        })
                    }
                ],
                chartOptions: {
                    chart: {
                        stacked: true,
                        events: {
                            selection: function (chart, e) {
                                console.log(new Date(e.xaxis.min))
                            }
                        },
                    },
                    colors: ['#ffa000', '#00E396', '#CED4DC'],
                    dataLabels: {
                        enabled: false
                    },
                    stroke: {
                        curve: 'smooth'
                    },
                    fill: {
                        type: 'gradient',
                        gradient: {
                            opacityFrom: 0.6,
                            opacityTo: 0.8,
                        }
                    },
                    legend: {
                        position: 'top',
                        horizontalAlign: 'left'
                    },
                    xaxis: {
                        type: 'datetime'
                    },
                }
            }
        },
        methods: {
            generateDayWiseTimeSeries: function (baseval, count, yrange) {
                var i = 0;
                var series = [];
                while (i < count) {
                    var x = baseval;
                    var y = Math.floor(Math.random() * (yrange.max - yrange.min + 1)) + yrange.min;

                    series.push([x, y]);
                    baseval += 86400000;
                    i++;
                }
                return series;
            }
        }
    }
</script>

<style scoped>

</style>
