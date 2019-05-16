<template>
  <div id="add-new-log">
    <h1>Add New Log</h1>
    <form>
      <input 
        type="text" 
        placeholder="Log title" 
        v-model="logTitle">
      <input 
        type="text" 
        placeholder="Log Message"
        v-model="logMessage">
      <ButtonComponent>Submit Log</ButtonComponent>
    </form>
  </div>

</template>

<script>
import ButtonComponent from './ButtonComponent.vue'


export default {
  name: 'AddNewLog',
  data: function (){
    return {
      logTitle: '',
      logMessage: ''
    }
  },
  components: {
    ButtonComponent
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
</style>
