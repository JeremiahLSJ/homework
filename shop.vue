<template>
  <div class="App">
    <table>
      <h4>欢迎光临_vue开发的收银系统_水果店</h4>
      <div>苹果10￥/斤，折扣8折</div>
      <span>请输入你要购买的斤数</span>
      <input type="number" value="0" v-model="value" />
      <br />
      <button @click="calculate">结账买单</button>
      <div>结账单：总价：{{ total }}￥元 折后价：{{ total * 0.8 }}￥元 省了：{{ total * 0.2 }}元</div>
    </table>
  </div>
</template>

<script>
export default {
  data () {
    return {
      value: '0',
      total: '0'
    }
  },
  methods: {
    calculate () {
      this.total = this.value * 10
    }
  }
}
</script>

<style>
.App {
  margin: auto;
}
table {
  text-align: center;
}
</style>
