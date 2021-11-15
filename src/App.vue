<template>
<div>
  <Header @added="addParticipant"/>
  <h1>
    
  </h1>

  <DataTable :participants="participants" />
  <ChartPie />
</div>
  
</template>

<script>

import Header from './components/Header.vue'
import DataTable from './components/DataTable.vue'
import ChartPie from './components/ChartPie.vue'



export default {
  name: 'App',
  components: {
    Header,
    DataTable,
    ChartPie
  },
  data(){
    return {
      participants: [],
    }
  },
  methods:{
    addParticipant(participant){
      this.participants.push(participant);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
