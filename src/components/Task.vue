<template>
    <div @dblclick="$emit('toggle-reminder',task.id)" :class="[task.reminder ? 'reminder' : '','tasks']">
        <h3>{{ task.text }}
            <i @click="$emit('delete-task',task.id)" class="fas fa-times"></i>
        </h3>
        <p>{{ task.day }}</p>
    </div>
</template>

<script>
export default {
    name:'Task',
    props:{
        task:Object
    },
}
</script>

<style scoped>
    .fas{
        color: red;
    }
    .tasks{
        background: #f4f4f4;
        margin: 5px;
        padding: 10px 20px;
        cursor:pointer;
    }
    .tasks.reminder{
        border-left: 5px solid green;
    }

    .tasks.h3{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
</style>