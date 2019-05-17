<template>
  <div id="add-new-log">
    <h1>Add New Log</h1>
    <form 
      class="form-container"
      @submit.prevent="createLogCard">
      <input 
        type="text" 
        placeholder="Log title" 
        v-model="logTitle">
      <input 
        type="text" 
        placeholder="Log Message"
        v-model="logMessage">
      <input
        type="submit"
        value="Submit Log">
    </form>
    <div v-if="cards.length">
      <div v-for="(card, index) in cards" :key="index">
        <LogCard :card="card" />
      </div>
    </div>
  </div>

</template>

<script>
import LogCard from './LogCard.vue'


export default {
  name: 'AddNewLog',
  components: {
    LogCard
  },
  data () {
    return {
      logTitle: '',
      logMessage: '',
      cards: []
    }
  },
  methods: {
    createLogCard(){
      this.cards.push({
        title: this.logTitle, 
        message: this.logMessage
      })
    }
  } 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.form-container{
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
