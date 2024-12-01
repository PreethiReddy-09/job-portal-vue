<template>
  <MyHeader appName="JOB PORTAL"/> 
  <JobList :jobs=jobs />
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import JobList from './components/JobList.vue'


export default{
  name: 'App',
  components:{
    MyHeader,
    JobList
  },
  data(){
    return {
      jobs: []
    }
  },
  methods:{
    async fetchjobs(){
      const res = await fetch('https://job-portal-node-v8kf.onrender.com/api');
      const data = await res.json()
      console.log(data)
      return data.jobs;
    }
  },
  async created(){
      this.jobs = await this.fetchjobs();
  }
}
</script>


<style>

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;

}

body {
  font-family: sans-serif;
}

#app{
  background-color:#808080
}

</style>
