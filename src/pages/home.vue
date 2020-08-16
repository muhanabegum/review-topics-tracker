<template>
  <div id="app">
    <AddTopic v-on:add-topic="addTopic" />
    <topics v-bind:topics="topics" v-on:del-topic="deleteTopic"/>
  </div>
</template>

<script>
import topics from '../components/topics'; 
import AddTopic from '../components/add-topic'; 
export default {
  name: 'Home',
  components:{ 
    topics, 
    AddTopic
  },
  data(){
    return {
      topics:[]
    }
  },
  methods:{
    deleteTopic(id){
      this.topics=this.topics.filter(topic=>topic.id !== id); 
    }, 
    addTopic(newTopic){
      this.topics = [...this.topics, newTopic]; 
    }
  }

}
</script>

<style>
  *{
    box-sizing: border-box;
    margin: 0; 
    padding: 0; 
  }

</style>
