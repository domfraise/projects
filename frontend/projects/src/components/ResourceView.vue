<template>
    <div id="timeline"></div>
</template>



<script>
    export default {
        name: "ResourceView",
    }

    import {GoogleCharts} from 'google-charts';

    //Load the charts library with a callback
    GoogleCharts.load(drawChart);

    function drawChart() {
        var container = document.getElementById('timeline');
        var chart = new GoogleCharts.api.visualization.PieChart(container);
        var dataTable = new GoogleCharts.api.visualization.DataTable();

        dataTable.addColumn({ type: 'string', id: 'President' });
        dataTable.addColumn({ type: 'date', id: 'Start' });
        dataTable.addColumn({ type: 'date', id: 'End' });
        dataTable.addRows([
            [ 'Washington', new Date(1789, 3, 30), new Date(1797, 2, 4) ],
            [ 'Adams',      new Date(1797, 2, 4),  new Date(1801, 2, 4) ],
            [ 'Jefferson',  new Date(1801, 2, 4),  new Date(1809, 2, 4) ]]);

        chart.draw(dataTable);
    }
</script>

<style scoped>

</style>