<template>
    <Hapag-Header />
    <div class="w-full p-4 flex" style="gap:1em;flex:1">
        <section id="left" class="flex-col" style="display:flex;flex: 0 0 auto;">
            <card title="Balance" value="312,312" secondaryTitle="Average Monthly" secondaryValue="336,699" />
            <card title="Recent Order" value="Crankshaft CNC" secondaryTitle="Charges" secondaryValue="450" />
            <category-chart />
        </section>
        <section id="right" style="gap:1em;flex:8">
            <section id="right-top">
                <ship-status />
                <no-of-goods-chart />
            </section>
            <section id="right-bottom"></section>
        </section>
    </div>
</template>

<script>
import HapagHeader from '../../components/Header/HeaderFile.vue';
import Card from '../../components/Cards/index.vue';
import ShipStatus from '../../components/ShipStatus/index.vue';
import CategoryChart from '../../components/Cards/CategoryChart.vue'
import NoOfGoodsChart from '../../components/Charts/NoOfGoodsChart.vue'
export default {
    components: {
        Card,
        HapagHeader,
        ShipStatus,
        CategoryChart,
        NoOfGoodsChart
    },
}
</script>

<style lang="scss" scoped>
</style>