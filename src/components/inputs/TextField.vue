<template>
    <va-input class="mb-4" v-model="value" :placeholder="placeholder" :typeof="type"/>
</template>

<script>
export default {
    name: 'TextField',
    props: {
        placeholder: {
            type: String,
            default: '',
        },
        type: {
            type: String,
            default: 'text',
        },
    },
}
</script>

<style scoped>
</style>