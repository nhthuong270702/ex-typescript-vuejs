<template>
    <ul>
        <li v-for="job in jobs" :key="job.id">
        <h2>{{job.title}} in {{job.location}}</h2>
        <div class="salary">
            <p>{{job.salary}} $</p>
        </div>
        <div class="description">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt officiis quidem facere deserunt! Repellendus, voluptates officia eum, sequi maiores, earum nemo ipsa asperiores unde id soluta mollitia a totam doloribus.</p>
        </div>
        </li>
    </ul>
</template>

<script lang="ts">
import Job from '@/types/jobs'
import { defineComponent, PropType } from 'vue'

export default defineComponent({
    name: 'job-list',
    props:{
        jobs:{
            type: Array as PropType<Job[]>,
            required: true
        }
    }
})
</script>

<style scoped>
    .salary{
        color: blue;
        font-weight: bold;
        font-size: 20px;
    }
    ul{
        list-style: none;
    }
    .description{
        font-size: 17px;
    }
    ul li{
        border: 1px solid black;
        margin: 5px;
        padding: 5px 30px;
         background-color: rgb(237, 223, 207);
    }
</style>
