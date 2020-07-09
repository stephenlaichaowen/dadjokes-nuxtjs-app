<template>
  <div>
    <SearchJokes @search-text="searchText" />
    <Joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke" />
  </div>
</template>

<script>
  import Joke from '@/components/Joke'
  import SearchJokes from '@/components/SearchJokes'


  export default {
    name: 'jokes',
    components: {
      Joke,
      SearchJokes
    },
    data() {
      return {
        jokes: []
      }
    },
    methods: {
      async searchText(text) {
        const config = {
        headers: {
          Accept: 'application/json'
        }
      }      
      try {
        const res = await this.$axios.get(`/search?term=${text}`, config)
        // return { jokes: res.data.results }
        this.jokes = res.data.results
      } catch (err) {
        console.log(err)
      }        }
    },
    asyncData(context) {
      const config = {
        headers: {
          Accept: 'application/json'
        }
      }      
      return context.app.$axios.$get('/search', config)
        .then(data => {
          return { jokes: data.results }
        })
    },
    head: {
      title: 'Dad Jokes',
      meta: [
        { hid: 'description', name: 'description', content: 'Best place for corny data jokes' }
      ]
    }
  }
</script>

<style scoped>

</style>