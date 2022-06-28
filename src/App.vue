<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-29 03:23:47
 * @LastEditors: sj
 * @LastEditTime: 2022-06-29 03:28:33
-->
<template>
  <div>
    <!-- 模拟实现v-model -->
    <input type="text" :value="val" @input="inputFn">
  </div>
</template>

<script>
export default {
 data(){
  return {
    val:''
  }
 },
 methods:{
  inputFn(e){
    this.val=e.target.value
  }
 }
}
</script>

<style>

</style>