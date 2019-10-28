<template>
  <div class="container">
    <h1>It`s {{ name }}</h1>
    <button @click="changeName">Not {{ name }}</button>
  </div>
</template>

<script>
export default {
  name: 'SearchForm',
  data: function () {
    return {
      name: 'Max'
    }
  },
  methods: {
    changeName: function () {
      this.name = this.name === 'Max' ? 'Julia' : 'Max'
    }
  }
}
</script>
<style scoped>
  div.container {
    width: 700px;
    margin: 20px;
    border: 2px solid green;
    border-radius: 20px;
  }
</style>
