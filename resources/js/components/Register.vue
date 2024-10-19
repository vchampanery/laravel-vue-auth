<template>
    <form @submit.prevent="register">
        <input v-model="name" type="text" placeholder="Name" required />
        <input v-model="email" type="email" placeholder="Email" required />
        <input v-model="password" type="password" placeholder="Password" required />
        <button type="submit">Register</button>
        <div v-if="error">{{ error }}</div>
    </form>
</template>

<script>
export default {
    data() {
        return {
            name: '',
            email: '',
            password: '',
            error: null,
        };
    },
    methods: {
        async register() {
            try {
                // Call the registration API
            } catch (err) {
                this.error = 'Registration failed';
            }
        },
    },
};
</script>