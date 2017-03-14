<template>
  <div>
    <mynav></mynav>
    <tab></tab>
    <p>haha</p>
    <p>你是个好人</p>
  </div>
</template>

<script>
  import Vue from "vue"
  import nav from "./component/nav.vue"
  import table from "./component/table.vue"
  Vue.component("mynav",nav);
  Vue.component("tab",table)
export default {

}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
  }
</style>
