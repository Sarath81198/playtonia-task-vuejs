<template>
    <div>
        <b-card bg-variant="light" text-variant="dark" :title="todo.title">
            <b-card-text class="text-secondary">
                For user {{ todo.userId }}
            </b-card-text>
            <b-card-text>
                <b class="text-success" v-if="todo.completed == true">Completed</b>
                <b class="text-warning" v-else-if="todo.completed == false">Yet to be completed</b>
            </b-card-text>
        </b-card>
    </div>
</template>

<script>
export default {
    name:"TodoItem",
    props: ["todo"]
}
</script>