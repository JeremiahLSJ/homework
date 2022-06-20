<template>
  <div>
    <form action="">
      <i v-for="item in arr" :key="item.id">
        <input type="checkbox" checked="item.checked" v-model="item.checked" />
        {{ item.name }}
      </i>
    </form>

    <ul>
      <li v-for="item in arr" :key="item.id" v-show="item.checked">{{ item.name }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data () {
    return {
      arr: [
        { id: 1, name: '科幻', checked: true },
        { id: 2, name: '喜剧', checked: true },
        { id: 3, name: '动漫', checked: true },
        { id: 4, name: '冒险', checked: true },
        { id: 5, name: '科技', checked: true },
        { id: 6, name: '军事', checked: true },
        { id: 7, name: '娱乐', checked: true },
        { id: 8, name: '奇闻', checked: true }
      ],
      hobby: []
    }
  }
}
</script>

<style></style>
