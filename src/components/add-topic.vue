<template>
    <div>
        <form @submit="addTopic">
            <input type="text" v-model="title" name="title" placeholder="Type in a topic...">
        </form>
    </div>
</template>

<script>
import {v4 as uuidv4} from 'uuid';  
export default {
    name: "AddTopic", 
    data(){
        return {
            title:'', 
            counter: 0
        }
    }, 
    methods:{
        addTopic(e){
            e.preventDefault(); 
            const newTopic = {
                id: uuidv4(), 
                title: this.title,
                completed: false
            }
            this.$emit('add-topic', newTopic); 
            this.title ='';  
        }
    }
}
</script>

<style scoped>
    form{
        display: flex; 
        height: 40px;
        justify-content: center; 
    }

    input[type="text"]{
        flex: 10; 
        border-radius: 2px; 
        border: 3px;
        padding: 12px 20px;
        background-color: #f4f4f4; 
    }

</style>