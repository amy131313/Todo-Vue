<template>
    <div @dblclick="$emit('toggle-reminder', task.id)" :class="[task.reminder ? 'reminder' : '', 'task']">
        <h4>{{ task.text }} 
            <i @click="this.$emit('delete-task', id)" class="fas fa-times"/>
        </h4>
        <p>{{ task.day }}</p>

    </div>
</template>

<script>
export default {
    name: 'Task',
    props: {
        task: Object
    },
}
</script>

<style scope>
.fas {
    color: red;
}
.task {
    background: #f4f4f4;
    margin: 5px;
    padding: 20x 20px;
    cursor: pointer;
}

.task.reminder {
    border-left: 5px solid green;
}

.task h3 {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>