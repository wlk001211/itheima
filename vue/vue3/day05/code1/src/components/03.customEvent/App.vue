<template>
  <div>
    <h1>App 根组件</h1>
    <p></p>
    <hr>
    <my-counter @countchange="getCount"></my-counter>
  </div>
</template>

<script>
import MyCounter from './Counter.vue'
export default {
name:'MyApp',
methods: {
  getCount(val){
    console.log('触发了自定义事件',val);
  }
},
components:{
MyCounter
}
}
</script>

<style>

</style>