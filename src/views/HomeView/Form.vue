<template>
    <div id="form">
        <div class="w-80 bg-white rounded-lg p-8 flex flex-col md:ml-auto w-full mt-10 md:mt-0 relative z-10 shadow-md">
            <h2 class="text-gray-900 text-lg mb-1 font-medium title-font">Welcome</h2>
            <p class="leading-relaxed mb-2 text-gray-600">
                Login to your account to get started.
            </p>
            <div class="relative mb-4">
                <label for="email" class="leading-7 text-sm text-gray-600">Email</label>
                <input id="email" v-model="email" type="email"
                    class="w-full bg-white rounded border border-gray-300 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-200 text-base outline-none text-gray-700 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out">
            </div>
            <div class="relative mb-4">
                <label for="password" class="leading-7 text-sm text-gray-600">Password</label>
                <input id="password" v-model="password" type="password"
                    class="w-full bg-white rounded border border-gray-300 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-200 text-base outline-none text-gray-700 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out">
            </div>
            <div v-show="!isValid" class="relative mb-4">
                <h6 class="leading-relaxed text-red-800 text-xs">Email or Password is incorrect</h6>
            </div>
            <button @click.prevent="submit"
                class="text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg"
                style="background-color: var(--secondary);">{{ isLoading ? 'Loading...' : 'Log In' }}</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Hapag-Form',
    data() {
        return {
            isLoading: false,
            isValid: true,
            email: 'admin@hapag.co',
            password: '12345678',
        };
    },
    methods: {
        submit() {
            console.log('Submit');
            if (this.validateCredentials()) {
                this.isValid = true;
                this.isLoading = true;
                setTimeout(() => {
                    this.isLoading = false;
                    this.$router.push('/dashboard');
                }, 1000);
            } else {
                this.isValid = false;
                return;
            }
        },
        validateCredentials() {
            return this.validateEmail(this.email) && String(this.email).trim() === "admin@hapag.co" && String(this.password).trim() === "12345678";
        },
        validateEmail(email) {
            return String(email)
                .toLowerCase()
                .match(
                    /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
                );
        }
    },
    components: {}
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