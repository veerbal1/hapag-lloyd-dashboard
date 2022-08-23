<template>
    <div class="w-full max-w-xs shadow-md p-6">
        <canvas id="category-chart" width="272" height="272">

        </canvas>
    </div>
</template>

<script>
import { Chart, registerables } from 'chart.js';
Chart.register(...registerables);
export default {
    name: 'CategoryChart',
    mounted: () => {
        const ctx = document.getElementById('category-chart').getContext('2d');
        new Chart(ctx, {
            type: 'doughnut',
            data: {
                labels: ['Pharmaceutical Products', 'Fruits', 'Paints', 'Juices', 'Dry Fruits'],
                datasets: [{
                    label: '# of Votes',
                    data: [1, 19, 3, 5, 2],
                    backgroundColor: ['#EE6082', '#F49E3F', '#F9CC53', '#52C0C0', '#339AF7'],
                    borderWidth: 1
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
                        text: 'Last 6 Months - No. of Containers'
                    }
                }
            }
        })
        console.log('Chart mounted', ctx)
    }
}
</script>

<style>
</style>