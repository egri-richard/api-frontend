<template>
  <User v-for="d in this.data" :key="d.name" :info="d" />
</template>

<script>
import User from './components/User.vue'

export default {
  name: 'App',
  components: {
    User
  },
  data() {
    return {
      data: Array
    }
  },
  created() {
    this.getUsers()
  },
  methods: {
      async getUsers() {
        try {
            const res = await fetch('http://10.4.18.51:8080/helloWorld')
            const data = await res.json()
            this.data = data
        } catch(error) {
          console.log(error)
        }
      }
  }
}

</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
