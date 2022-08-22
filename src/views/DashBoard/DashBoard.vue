<template>
    <Hapag-Header />
    <div class="w-full p-4 flex" style="gap:1em;flex:1">
        <section id="left" class="flex-col" style="display:flex;flex: 0 0 auto;">
            <card title="Balance" value="312,312" secondaryTitle="Average Monthly" secondaryValue="336,699" />
            <card title="Active Order" value="CNC Crank Grinding" secondaryTitle="Charges" secondaryValue="450" />
        </section>
        <section id="right" style="gap:1em;flex:8">
            <section id="right-top">Right Top</section>
            <section id="right-bottom">Right Bottom</section>
        </section>
    </div>
</template>

<script>
import HapagHeader from '../../components/Header/HeaderFile.vue';
import Card from '../../components/Cards/index.vue';
export default {
    components: {
        Card,
        HapagHeader,
    },
}
</script>

<style lang="scss" scoped>
</style>