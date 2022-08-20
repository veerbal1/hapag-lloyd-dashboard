<template>
    <div id="form">
        <H1Vue text="Welcome" />
        <text-field placeholder="Email" v-model="email" type="email" messages="Email: admin@hapag.co" />
        <text-field placeholder="Password" v-model="password" type="password" messages="Password: 12345678"/>
        <va-button color="warning" class="mr-4 mb-2" :rounded="false">Log In</va-button>
        <va-button v-show="false" color="warning" class="mr-4 mb-2" :rounded="false" loading size="medium">Log In
        </va-button>
    </div>
</template>

<script>
import TextField from '../../components/inputs/TextField.vue';
import H1Vue from '../../components/typography/H1Vue.vue';
export default {
    name: 'Hapag-Form',
    data() {
        return {
            email: 'admin@hapag.co',
            password: '12345678',
        };
    },
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