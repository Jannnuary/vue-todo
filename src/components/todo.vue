<template>
  <div class="todo">
    <div class="title">{{header}}</div>
    <div class="add">
      <input type="text" />
        <img alt="addBt" src="../assets/add.png" @click="handerAdd"/>
    </div>
    <ul class="unfinished">
      <li v-for="item in unfinishedTodos" @click="change(item)" :key="item" class>
        <input type="radio" :checked="item.status === 'finished'" />
        <label>{{ item.desc }}</label>
      </li>
    </ul>
    <ul class="finished">
      <li v-for="item in finishedTodos" :key="item">
        <input @click="change(item)" type="radio" id="index" :checked="item.status === 'finished'" />
        <label for="index">{{ item.desc }}</label>
      </li>
    </ul>

  </div>
</template>
<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
export default class HelloWorld extends Vue {}
</script>
<style lang="less">
</style>
