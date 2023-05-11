<template>
    <h1>
        Get Input field Value
    </h1>
    <!--   -->
    <form  name="form1">
        

        <label>Username : </label>
        <input  type="text" name= "email" placeholder="Email/Username" v-model="email" /> <br />
        <label>Password : </label>
        <input type="password" name="Password" placeholder="Password" v-model="password" /><br /> 

        <h2>Technologies</h2>
        <label for="java">Java</label>
        <input type="checkbox" value="java" id="java" v-model="technology"/> <br />

        <label for="node">Node</label>
        <input type="checkbox" value="node" id="node" v-model="technology"/> <br />

        <label for="php">PHP</label>
        <input type="checkbox" value="php" id="php" v-model="technology"/> <br />

        <h3>Technologies: {{technology}}</h3>

        <h1>Profession</h1>
        <label for="profession">Student</label>
        <input type="radio" value="student" id="profession" v-model="profession"/> <br />

        <label for="employee">Employee</label>
        <input type="radio" value="employee" id="employee" v-model="profession"/> <br />

        <label for="unemployed">Unemployed</label>
        <input type="radio" value="unemployed" id="unemployed" v-model="profession"/> <br />

        <h3>Profession: {{profession}}</h3>

        <button type="button" v-on:click="getData()">Get Data</button>
        
    </form>

    <!-- <h1>{{ username }}{{ getName() }}</h1>
    <h1>Email: {{getEmail("titus.sid91@gmail.com")}}</h1>
    <h1>Data-name: {{getData().name}}</h1>
    <h1>Data-email: {{ getData().email }}</h1>  -->


    <button v-on:click="getPlus()"> Plus {{ count }}</button>
    <button v-on:click="getMinus()"> Minus {{ count }}</button>
    <h2>Love you {{3000 + count}}</h2>
</template>

<script>
import HelloWorld from './HelloWorld.vue';


    export default {
    data() {
        return {
            data: 500,
            count: 0,
            username: "Titus",
            email: "abc@xyz.com",
            password: "123456",
            getEmail(x) {
                return x;
            },
            technology: [],
            profession:"",
            HelloWorld
        };
    },
    methods: {
        getData() {
            console.log("values:", this.email, this.password, this.technology, this.profession);
        },
        getName() {
            return " Siddique";
        },
        getPlus() {
            this.count++;
        },
        getMinus() {
            this.count--;
        }
    },
}
</script>


<style scoped>
h1{
    color: red;
}
</style>