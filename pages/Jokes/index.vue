<template>
    <div>
        <Joke v-for="joke in jokes" :key="joke.id"
        :id="joke.id" :joke="joke.joke"/>
    </div>
</template>

<script>
import axios from 'axios';
import Joke from '../../components/Joke';

export default {
  components: {
    Joke
  },
  data(){
    return{
      jokes:[]
    }
  },
  async created(){
    const config = {
      headers:{
        Accept: "application/json"
      }
    };

    try {
      const res = await axios.get("https://icanhazdadjoke.com/search",config);
    
      this.jokes = res.data.results;
    }catch (err) {
      console.log(err);
    }
  },
    head: {
    titleTemplate: 'My Nuxt JS App - Jokes',
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },

      // hid is used as unique identifier. Do not use `vmid` for it as it will not work
      { hid: 'description', name: 'description', content: 'A list of dad jokes' }
    ]
  }
}

</script>

<style>

</style>