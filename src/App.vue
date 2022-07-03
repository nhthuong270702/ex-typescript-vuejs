<template>
  <div class="app">
    <!-- <p>{{name}} - {{age}}</p>
    <button @click="changeName('truc')">Change Name</button>
    <button @click="changeAge('19')">Change Age</button> -->

    <!-- <p v-for="job in jobs" :key="job.id">{{job.location}}</p> -->

    <job-list :jobs="jobs"/>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRef, toRefs } from 'vue';
import Job from './types/jobs';
import JobList from './components/JobList.vue'

export default defineComponent({
  name: 'App',
  components: {
    JobList
  },
  setup(){
// const state = reactive({
//   name: 'Thuong',
//   age: 20 as number | string
// })
// return {...toRefs(state)}
//=======================
// const name = ref('Thuong')
// const age = ref<number | string>(20)
// return {name, age}
//=======================
const jobs = ref<Job[]>([
  {title: 'title1', location: 'thua thien hue1', salary: 50000, id: 1},
  {title: 'title2', location: 'thua thien hue2', salary: 60000, id: 2},
  {title: 'title3', location: 'thua thien hue3', salary: 70000, id: 3},
  {title: 'title4', location: 'thua thien hue4', salary: 80000, id: 4},
  {title: 'title5', location: 'thua thien hue5', salary: 90000, id: 5},
  {title: 'title6', location: 'thua thien hue6', salary: 10000, id: 6},
  {title: 'title7', location: 'thua thien hue7', salary: 30000, id: 7},
])

return {jobs}
  },
  methods:{
    // changeName(name: string){
    //   this.name = name
    // },
    // changeAge(age: number | string){
    //   this.age = age
    // }
  }
});
</script>

<style>
</style>
