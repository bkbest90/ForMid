<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view></router-view>
    <table align="center">
      <tr>
        <td colspan="3"><img src="currentImage" style="width:304px;height:228px;"></td>
      </tr>
      <tr>
        <td><button @click="back" :disabled="page === 1"><</button></td>
        <td>{{page}}</td>
        <td><button @click="next" :disabled="page === 26">></button></td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      page: 1
    }
  },
  methods: {
    next: function () {
      this.page += 1
    },
    back: function () {
      this.page -= 1
    }
  },
  computed: {
    currentImage () {
      return 'http://bill.sellsuki.com/cartoon/' + this.page + '.jpg'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
