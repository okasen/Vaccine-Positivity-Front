<template>
  <Form/>
  <Read/>
</template>

<script>
import Form from './components/Form.vue'
import Read from './components/Read.vue'

export default {
  name: 'App',
  components: {
    Form,
    Read
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
