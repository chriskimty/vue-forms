<template>
    <form>
        <label>Email</label>
        <input type="email" required v-model="email">
        <!-- ^2-way data binding - technically 'email' could be called anything-->
        <!-- what does this mean? values are bound 2 ways b/n template inputs and the component data itself  -->

        <label>Password</label>
        <input type="password" required v-model="password">

        <label>Role: </label>
        <select v-model="role">
            <option value="developer">Web Developer</option>
            <option value="designer">Web Designer</option>
        </select>

        <!-- two ways of creating a checkbox -->
        <div class="terms">
            <input type="checkbox" v-model="terms" required>
            <label>Accept terms and conditions</label>
        </div>

        <!-- another type of checkbox - we use an array and not boolean (array to contain the ones we checked) -->
        <!-- <div>
            <input type="checkbox" value="chris" v-model="names">
            <label>Chris</label>
        </div>
        <div>
            <input type="checkbox" value="sang" v-model="names">
            <label>Sang</label>
        </div>
        <div>
            <input type="checkbox" value="chabs" v-model="names">
            <label>Chabs</label>
        </div> -->
    </form>
    <!-- to see if we are actually tracking -->
    <p>Email: {{ email  }}</p>
    <p>Password: {{ password  }}</p>
    <p>Role: {{ role  }}</p>
    <p>Terms accepted: {{ terms }}</p>
    <!-- <p>Names: {{ names }}</p> -->
</template>

<script>
export default {
    data() {
        return {
            // when the user types in the input, the '' gets updated with the value they type in - to keep track. so how to sync it together?  (v-model 2 way data binding)
            email: '',
            password: '',
            role: 'designer',
            terms: false
            // names: []
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
    input, select {
        display: block;
        padding: 10px 6px;
        width: 100%;
        box-sizing: order-box;
        border: none;
        border-bottom: 1px solid #ddd;
        color: #555;
    }
    input[type="checkbox"]{
        display: inline-block;
        width: 16px;
        margin: 0 10px 0 0;
        position: relative;
        top: 2px;
    }
</style>