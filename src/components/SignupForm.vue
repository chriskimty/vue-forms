<template>
    <form>
        <label>Email</label>
        <input type="email" required v-model="email">
        <!-- ^2-way data binding - technically 'email' could be called anything-->

        <label>Password</label>
        <input type="password" required v-model="password">
    </form>

    <!-- to see if we are actually tracking -->
    
</template>

<script>
export default {
    data() {
        return {
            // when the user types in the input, the '' gets updated with the value they type in - to keep track. so how to sync it together?  (v-model 2 way data binding)
            email: '',
            password: ''
        }
    }
}
</script>

<style>
    form {
        max-width: 420px;
        margin: 30px auto;
        background: white;
        text-align: left;
        padding: 40px;
        border-radius: 10px;
    }
    label {
        color: #aaa;
        display: inline-block;
        margin: 25px 0 15px;
        font-size: 0.6em;
        text-transform: uppercase;
        letter-spacing: 1px;
        font-weight: bold;
    }
    input {
        display: block;
        padding: 10px 6px;
        width: 100%;
        box-sizing: order-box;
        border: none;
        border-bottom: 1px solid #ddd;
        color: #555;
    }
</style>