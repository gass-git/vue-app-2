<template>
    <h1>job title: {{ props.title }}</h1>
    <router-link v-bind:to="{ name: 'jobs' }"> 
        Go back to jobs 
    </router-link>
</template>


<script setup>
    import {useRoute} from 'vue-router'
    import {defineProps} from 'vue'

    const route = useRoute()
    const props = defineProps({title: String}) 
</script>
