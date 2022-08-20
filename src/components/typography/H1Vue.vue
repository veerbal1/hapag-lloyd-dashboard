<template>
    <h1>{{ text }}</h1>
</template>

<script>
export default {
    name: 'H1Vue',
    props: ["text"]
}
</script>

<style scoped>
h1 {
    text-transform: uppercase;
    font-weight: 700;
    font-size: 2em;
    margin-bottom: 0.5em;
}
</style>