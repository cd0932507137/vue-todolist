<template>
  <div class="view">
    <h1 class="title">{{ title }}</h1>
    <input v-model="newStr" @keyup.enter="addData">
    <ul>
      <li v-for="item in items" :key="item.text" v-bind:class="{finish:item.isFinished}" @click="toggleFinish(item)">
        {{ item.text }}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'List',
  data () {
    return {
      title: 'TodoList',
      items: [
        {
          text: '今天晚上跑步',
          isFinished: false
        },
        {
          text: '明天洗衣服',
          isFinished: true
        }
      ],
      newStr: ''
    }
  },
  methods: {
    toggleFinish: function (item) {
      console.log(item)
      item.isFinished = !item.isFinished
    },
    addData: function () {
      this.items.push({
        text: this.newStr,
        isFinished: false
      })
      // 清空輸入框
      this.newStr = ''
    }
  }
}
</script>
<style>
.view {
  width: 400px;
  border: 1px solid gray;
  margin: 20px auto;
}
.view .title {
    border-bottom: 1px solid gray;
}
.view ul li {
    margin: 10px 0;
    list-style: none;
}
.finish {
    color: gray;
    text-decoration: line-through;
}
</style>
