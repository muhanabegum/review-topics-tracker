<template>
    <header class="header">
        <h1><font-awesome-icon :icon="['fas', 'graduation-cap']" /> EXAM STUDY SHEET TRACKER <font-awesome-icon :icon="['fas', 'graduation-cap']" /></h1> 
        <div id="nav">
            <router-link to="/">Review Topics List</router-link>||
            <router-link to="/about">Learn More</router-link>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Lato'); 
    .header{
        background: #abbbaa; 
        text-align: center; 
        padding: 10px;
        font-family: "Lato"; 
        font-size: 20px; 
        font-weight: 800; 
    }

    .header a{
        color:black; 
        padding-right: 5px; 
        font-size: 20px;
        font-family: "Lato";
    }

</style>


