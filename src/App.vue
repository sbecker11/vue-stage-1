<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <JunkerComponent :msg="message"/>
  <HelloWorld :msg="message"/>
  <JunkerComponent :msg="message"/>
  <input type="text" v-model="message" />
  <button @click="alertMessage">Alert</button>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import JunkerComponent from './components/JunkerComponent.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    JunkerComponent
  },
  data() {
    return {
      message: "Howdy Pard'ner"
    }
  },
  methods: {
    alertMessage(){
      alert(this.message)
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
