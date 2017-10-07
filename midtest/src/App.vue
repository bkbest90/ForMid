<script src="https://unpkg.com/vue">

</script>
<template>
  <div>
    <div>
      <h1>{{result}}</h1>
      <button @click="s()">+</button>
      <button @click="aa()">-</button>
  </div>
    <div class="box" :style="color"></div>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      result: 0
    }
  },
  methods: {
    s: function () {
      this.result += 1
    },
    aa: function () {
      this.result -= 1
    }
  }
}
</script>

<style>

</style>
