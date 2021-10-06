<template>
    <button @click="this.$emit('show-addTask')" :style="{ background: color }" class="btn">{{text}}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String, 
        color: String
    },
    methods: {
        onClick() {
            this.$emit('show-addTask')
        }
    }
}
</script>