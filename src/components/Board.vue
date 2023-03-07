<script setup>
const musicList = [
  {title: "榜樣", score: 8, suggestion: true},
  {title: "病變", score: 5, suggestion: false},
  {title:"備胎", score: 7, suggestion: true}
]
</script>

<template>
<div class="whiteBoard">
  <h1>{{title}}</h1>
  <a v-bind:href="noteLink">this is my note Link which used v-bind </a>
  <ul>
    <li v-for="(music, index) in musicList" v-bind:key="music">
      <input type="checkbox" v-bind:checked="music.suggestion">
      {{index+1}}: {{music.title}} with score: {{music.score}}
    </li>
  </ul>

</div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Board',
  props:{
    title: String,
    noteLink: String,
  }
}
</script>

<style scoped>

</style>
