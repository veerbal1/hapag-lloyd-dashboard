<template>
    <div id="form">
        <H1Vue text="Welcome" />
        <text-field />
    </div>
</template>

<script>
import TextField from '../../components/inputs/TextField.vue';
import H1Vue from '../../components/typography/H1Vue.vue';
export default {
    name: 'Hapag-Form',
    components: {
        TextField,
        H1Vue,
    }
}
</script>

<style>
#form {
    width: 100%
}
</style>