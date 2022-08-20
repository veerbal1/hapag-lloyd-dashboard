<template>
    <div id="form">
        <H1Vue text="Welcome" />
        <text-field placeholder="Email" type="text" />
        <text-field placeholder="Password" type="password" />
        <va-button color="warning" class="mr-4 mb-2" :rounded="false">Log In</va-button>
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
    width: 100%;
    flex-direction: column;
    display: flex;
    justify-content: center;
    align-items: flex-start;
}
</style>