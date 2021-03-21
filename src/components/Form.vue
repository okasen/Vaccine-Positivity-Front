<template>
<span>Tell us your experience:</span>
<p style="white-space: pre-line;">{{ name }}</p>
<p style="white-space: pre-line;">{{ message }}</p>
<p style="white-space: pre-line;">{{ location }}</p>
<textarea v-model="name" placeholder="add your name"></textarea>
<textarea v-model="message" placeholder="add your experience"></textarea>
<textarea v-model="location" placeholder="add your general location"></textarea>
<button v-on:click="submitExperience(name, message, location)">Submit</button>
</template>

<script>
const axios = require('axios');

export default {
  name: 'Form',
  methods: {
    submitExperience(namePost, expPost, localePost){
      axios.post('http://localhost:3000/submissions', {
        name: namePost,
        experience: expPost,
        location: localePost,
      })
      .then(function (response) {
        console.log(response);
      })
      .catch(function (error) {
        console.log(error);
      });

    }
  }
}


</script>

<style>
</style>
