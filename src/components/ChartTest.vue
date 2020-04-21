<template>
    <div class="chart">
        <div id="main" ref="main" style="height: 100%"></div>
    </div>
</template>
<script>
    import echarts from 'echarts';

    export default {
        name: 'lineChart',
        data() {
            return {

            };
        },
        mounted() {
            const myChart = echarts.init(this.$refs.main);

            myChart.setOption({
                title: {
                    text: 'ECharts entry example'
                },
                tooltip: {},
                xAxis: {
                    data: ['shirt', 'cardign', 'chiffon shirt', 'pants', 'heels', 'socks']
                },
                yAxis: {},
                series: [{
                    name: 'sales',
                    type: 'bar',
                    data: [5, 20, 36, 10, 10, 20]
                }]
            });
        },
    }

</script>
<style>
    .chart{
        width: 100%;
        height: 300px;
    }

</style>