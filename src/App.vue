<template>
 <h1>Kismat kc</h1>
 <button @click="checkStatus" :disabled="isPlaying">Play</button>
 <Block v-if="isPlaying" :delay="delay" />
</template>

<script>
import Block from "./components/Block.vue"
export default {
  name: 'App',
  components: {
    Block
  },
  data(){
    return{
  isPlaying: false,
   delay: null

    }
  },
  methods: {
    checkStatus(){
this.isPlaying = true
this.delay = 2000 + Math.random() * 5000

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
  color: #444;
  margin-top: 60px;
}
</style>
