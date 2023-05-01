<template>
    <div class="nav">
        <router-link to="/">Home</router-link>
        <router-link to="Add">Add Restaurant</router-link>
        <a v-on:click="logout" href="#">Logout</a>
    </div>
</template>

<script>
export default{
    name:'Header',
    methods:{
        logout(){
            localStorage.clear();
            this.$router.push({name:'Login'})
        }
    }
}
</script>

<style>
.nav{
    background-color: #e7750b;
    overflow: hidden;
}
.nav a{
    float: left;
    text-align: center;
    padding: 16px 14px;
    text-decoration: none;
    font-size: 16px;
    color: #f2f2f2;
    margin: 4px 5px;
}
.nav a:hover{
    background-color: #ddd;
    color: #222;
}
</style>