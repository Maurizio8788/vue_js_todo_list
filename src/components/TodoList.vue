<template lang="">
    <div>
        <div v-for="task in tasks" v-bind:key="task.id">
            <TodoListItem @toggle-reminder="$emit('toggle-reminder', task.id)" v-bind:task="task" @delete-task="$emit('delete-task', task.id)" />
        </div>
    </div>
</template>
<script>
import TodoListItem from "./TodoListItem.vue"
export default {
    name:"TodoList",
    components:{
        TodoListItem
    },
    props:{
        tasks:Array
    },
    emits:['delete-tasks', 'toggle-reminder']
}
</script>
<style lang="css">
   
</style>