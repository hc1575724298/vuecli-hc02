<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-29 03:23:47
 * @LastEditors: sj
 * @LastEditTime: 2022-06-29 03:33:48
-->
<template>
  <div>
    <h1>{{ msg}}</h1>
    <button @click="fn">翻转</button>
    <!-- 模拟实现v-model -->
    <input type="text" :value="val" @input="inputFn">
  </div>
</template>

<script>
export default {
 data(){
  return {
    msg: 'Hello, world!',
     val:''
  }
 },
 methods:{
  fn(){
    this.msg=this.msg.split('').reverse().join('')
  },
  inputFn(e){
    this.val=e.target.value
  }
 },
}
</script>

<style>

</style>