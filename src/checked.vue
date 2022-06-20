<template>
  <div>
    <form action="">
      <i v-for="(item,index) in arr" :key="index">
        <input type="checkbox" :value="arr[index]" v-model="hobby" />
        {{ arr[index] }}
      </i>
    </form>

    <ul>
      <li v-for="(item,index) in hobby" :key="index">
        {{ hobby[index] }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data () {
    return {
      arr: ['科幻', '喜剧', '动漫', '冒险', '科技', '军事', '娱乐', '奇闻'],
      hobby: []
    }
  }
}
</script>

<style></style>
