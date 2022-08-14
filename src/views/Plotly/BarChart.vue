<template>
    <div id='BarChart'>
    </div>
</template>
<script>

import Plotly from 'plotly.js-dist';
//import * as d3 from "d3";

export default {
    name: 'BarChart',
    data: () => ({

    }),
    mounted() {
        this.getBarChart()
        console.log()

    },
    methods: {
        getBarChart() {
            var data = [{
                values: [19, 26, 55],
                labels: ['Residential', 'Non-Residential', 'Utility'],
                type: 'pie'
            }];

            var layout = {
                height: 400,
                width: 500
            };

            var config = { responsive: true }
            Plotly.newPlot("BarChart", data, layout, config)
        }

    }

}

</script>


<style>

</style>