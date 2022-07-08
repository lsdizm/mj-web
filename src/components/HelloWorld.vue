<template>
  <div class="hello">
    <h1>API 호출후 data적재</h1>
    <h1>마지막호출일 : {{ lastMigratedData }}</h1>
    <ul>
      <li>
        <button v-on:click="onTest">API 호출 TEST</button>
      </li>
      <li>
        <button v-on:click="onMigrateData">적재</button>
      </li>
    </ul>
      <h1>상태 : {{ message }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: function () {
    return {
      lastMigratedData: '없음',
      message: ''
    }
  },
  methods: {
    onTest: function () {
      this.$axios.get('https://jsonplaceholder.typicode.com/users').then(response => {
        console.log('### response: ' + JSON.stringify(response))
        this.message = response.data
      }).catch(error => {
        console.log(error)
      })
    },

    onMigrateData: function () {
      this.$axios.get('https://localhost:7030/WeatherForecast').then(response => {
        console.log('### response: ' + JSON.stringify(response))
        this.message = response.data
      }).catch(error => {
        console.log(error)
      })
    }
  }
}
</script>

<style scoped>
h1, h2 {
  font-weight: normal;
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
