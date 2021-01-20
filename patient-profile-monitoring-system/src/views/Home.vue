<template>
  <div class="home container mx-auto">
    <div class="text-center">
      <img alt="Vue logo" src="../assets/logo.png" />
      <h1>Patient Profile Monitoring System</h1>
      <button class="btn btn-danger" v-on:click="getData()">Get Data</button>
    </div>

    <ul class="list-group">
      <li class="list-group-item mb-2 shadow" v-for="i in info" :key="i.id">
        <h4><span class="badge badge-danger">{{ i.id }}</span> : {{ i.title }}</h4>
        <br>
        <p class="text-justify">
          {{ i.summary }}
        </p>
      </li>
    </ul>
  </div>

</template>

<script>
// @ is an alias to /src
import axios from 'axios'

export default {
  name: "Home",
  data: () => ({
    info:[]
  }),
  methods:{
    async getData(){
      let API = 'http://127.0.0.1:3000/events'
      await axios.get(API)
      .then(res => {
          let val  = res.data
          this.info = val
          // console.log(val)
      })
      .catch(function (error) {
          console.log(error);
      })
    }
  },
};
</script>
