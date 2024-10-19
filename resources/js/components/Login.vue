<template>
    <form @submit.prevent="login">
        <input v-model="email" type="email" placeholder="Email" required />
        <input v-model="password" type="password" placeholder="Password" required />
        <button type="submit">Login</button>
        <div v-if="error">{{ error }}</div>
    </form>
</template>

<script>
export default {
    data() {
        return {
            email: '',
            password: '',
            error: null,
        };
    },
    methods: {
        async login() {
            try {
                // Call the login API
            } catch (err) {
                this.error = 'Login failed';
            }
        },
    },
};
</script>