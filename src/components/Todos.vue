<template>
<div>
    <b-container>
        <div v-for="todo in todos" v-bind:key="todo.id">
            <TodoItem v-bind:todo="todo"/>
            <br>
        </div>
    </b-container>
    
</div>
</template>

<script>
import TodoItem from "./TodoItem.vue"

export default {
    name:"Todos",
    props:["todos"],
    components:{
        TodoItem
    }
}
</script>