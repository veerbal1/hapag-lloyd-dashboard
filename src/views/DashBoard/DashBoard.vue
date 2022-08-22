<template>
    <Hapag-Header />
    <div class="w-full p-4 flex" style="gap:1em;flex:1">
        <section id="left">
            <balance-card />
        </section>
        <section id="right" style="gap:1em;flex:5">
            <section id="right-top">Right Top</section>
            <section id="right-bottom">Right Bottom</section>
        </section>
    </div>
</template>

<script>
import HapagHeader from '../../components/Header/HeaderFile.vue'
import BalanceCard from '../../components/Cards/Balance.vue'
export default {
    components: {
        BalanceCard,
        HapagHeader
    }
}
</script>

<style lang="scss" scoped>
</style>