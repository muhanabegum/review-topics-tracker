<template>
    <div class="topic-item" v-bind:class="{'is-complete':topic.completed}">
        <p> 
            <input type="checkbox" v-on:change="markComplete">  
            {{topic.title}} 
            <button @click="$emit('del-topic', topic.id)" class="delete-button">Done! <font-awesome-icon :icon="['fas', 'check-square']" /></button>
            <select v-model="selected" class="confidence-level-button">
                <option disabled value="">Confidence Level</option>
                <option>1</option>
                <option>2</option>
                <option>3</option>
                <option>4</option>
                <option>5</option>
              </select>
        </p>
    </div>
</template>

<script>
export default {
    name: "TopicItem",
    props: ["topic"],
    methods: {
        markComplete() {
            this.topic.completed = !this.topic.completed;        
        }
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Lato'); 

    .topic-item{
        background: #c0dcc0; 
        padding: 10px; 
        border-bottom: 2px solid white ;
        text-align: left; 
        font-family: "Lato"; 
        font-size: 17px; 
        font-weight: 600; 
    }

    .is-complete{
        text-decoration: line-through;  
    }

    .delete-button{
        background: #238f23; 
        color: white; 
        padding: 5px 10px; 
        cursor: pointer; 
        float: right; 
        border: none; 
        font-size: 12px;
    }

    .confidence-level-button{
        float: right; 
        left: 20%; 
        text-align: center; 
        padding: 3px; 
    }
</style>