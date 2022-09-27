<template>
        <table>
            <tr>
                <th>job title</th>
                <th>details</th>
            </tr>
            <tr v-for="job in jobs" :key="job.id">
                <td>
                    <router-link v-bind:to="{ name:'jobs details', params:{ title: job.title } }">
                        {{ job.title }}
                    </router-link>
                </td>
                <td>
                    {{ job.details }}
                </td>
            </tr>
        </table>
</template>

<script setup>
import {ref} from 'vue'

    const jobs = ref([
        {id: 1, title: 'Junior Software Engineer', details: 'lorem ipsum'},
        {id: 2, title: 'Senior Software Engineer', details: 'lorem ipsum'},
        {id: 3, title: 'UX designer', details: 'lorem ipsum'}
    ])
</script>

<style scoped>
    table{
        margin:0 auto;
    }
    th{
        background:rgb(44, 166, 214);
        color:white;
        text-transform: uppercase;
    }
    th, td{
        border:1px solid rgb(215, 215, 215);
        padding:8px 30px 8px 30px;
    }
</style>