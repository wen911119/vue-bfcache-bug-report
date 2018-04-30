<template>
  <div class="hello">
      <div class="item" v-for="item in items" :key="item">
        {{item}}
      </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      items: []
    }
  },
  mounted() {
    for (let i = 1; i < 10; i++) {
      this.items.push(i)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  height: 100%;
  overflow: auto;
  -webkit-overflow-scrolling: touch;
}
.item {
  height: 300px;
  margin-bottom: 50px;
  background-color: #ccc;
  line-height: 300px;
  text-align: center;
}
</style>
