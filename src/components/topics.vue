<template>
    <div>
        <div v-bind:key="topic.id" v-for="topic in topics">
            <TopicItem v-bind:topic="topic" v-on:del-topic="$emit('del-topic', topic.id)"/>
        </div>
    </div>
</template>

<script>
import TopicItem from './topic-item.vue'; 
export default {
    name: "Topics",
    components:{
        TopicItem
    }, 
    props: ["topics"]
}
</script>

<style scoped>

</style>
