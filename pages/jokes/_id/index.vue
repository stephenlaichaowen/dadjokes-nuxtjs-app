<template>
  <div>
    <!-- {{ $route.params.id }} -->
    <nuxt-link to="/jokes">Back to Jokes</nuxt-link>
    <h2>{{ joke }}</h2>
    <hr>
    <!-- <small>Joke ID: {{ $route.params.id }}</small> -->
    <small>Joke ID: {{ $route.params.id.replace("'", '') }}</small>
  </div>
</template>

<script>
  export default {
    async asyncData(context) {
      const config = {
        headers: {
          Accept: 'application/json'
        }
      }      

      const newId = context.params.id.replace("'", '') 
      try {
        const data = await context.app.$axios.$get(`/j/${newId}`, config)
        return { joke: data.joke }
      } catch (err) {
        console.log(err)
      }  
    },
    head: {
      title: 'single joke',
      meta: [
        { hid: 'description', name: 'description', content: 'Best place for corny data jokes' }
      ]
    }
  }
</script>

<style scoped>

</style>