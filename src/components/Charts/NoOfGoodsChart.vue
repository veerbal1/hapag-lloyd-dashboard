<template>
    <div class="w-full p-6 relative flex flex-col justify-center items-center">
        <canvas id="no-of-goods-chart" width="100%" height="250">

        </canvas>
    </div>
</template>

<script>
import { Chart, registerables } from 'chart.js';
Chart.register(...registerables);
export default {
    name: 'NoOfGoodsChart',
    mounted: () => {
        const ctx = document.getElementById('no-of-goods-chart').getContext('2d');
        new Chart(ctx, {
            type: 'line',
            data: {
                labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
                datasets: [{
                    label: 'Pharmaceutical Products',
                    data: [197, 455, 397, 464, 747, 765, 163, 668, 0, 0, 0, 0],
                    borderColor: '#EE6082',
                    backgroundColor: '#EE6082'
                }, {
                    label: 'Fruits',
                    data: [58, 487, 744, 727, 72, 946, 451, 235, 0, 0, 0, 0],
                    borderColor: '#F49E3F',
                    backgroundColor: "#F49E3F"
                }, {
                    label: 'Paints',
                    data: [890, 680, 714, 3, 909, 53, 500, 427, 0, 0, 0, 0],
                    borderColor: '#F9CC53',
                    backgroundColor: "#F9CC53"
                }, {
                    label: 'CNC Machines',
                    data: [942, 911, 570, 490, 273, 844, 638, 382, 0, 0, 0, 0],
                    borderColor: '#52C0C0',
                    backgroundColor: "#52C0C0"
                }, {
                    label: 'Dry Fruits',
                    data: [531, 435, 264, 308, 261, 262, 106, 635, 0, 0, 0, 0],
                    borderColor: '#339AF7',
                    backgroundColor: "#339AF7"
                }]
            },
            options: {
                responsive: true,
                plugins: {
                    legend: {
                        position: 'top',
                    },
                    title: {
                        display: true,
                        text: 'No. of Containers ordered - Category Wise',
                        position: "top"
                    }
                }
            },
        })
    }
}
</script>

<style>
</style>