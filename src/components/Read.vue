<template>
<p>testing...</p>
<div class="horizontal">
  <div class="experience vertical" v-for="items in experiences" :key="items">
    <p><b>Name: </b>{{ items.name }}</p>
    <p><b>Their experience:</b></p>
    <p> {{ items.experience }}</p>
    <p><b>Located: </b>{{ items.location }}</p>
  </div>
</div>
</template>

<script>
const axios = require('axios');

export default {
  name: "Read",
  data() {
    return{
    experiences: []
    }
  },
  mounted() {
      axios.get("http://localhost:3000/approved").then(response => {
        this.experiences = response.data
      })
  }
}

</script>

<style>
.horizontal{
  display: flex;
  flex-direction: row;
}
.experience{
  text-align: left;
  padding: 10px;
}
</style>
