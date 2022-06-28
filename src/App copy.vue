<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-29 02:13:09
 * @LastEditors: sj
 * @LastEditTime: 2022-06-29 02:13:09
-->
<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-29 01:19:27
 * @LastEditors: sj
 * @LastEditTime: 2022-06-29 02:03:13
-->
<template>
  <div>
    <!-- 1. 插值表达式 {{}} -->
    <h1> {{ msg }}</h1>
    <h1> {{obj.name }}{{  obj.age>18? '成年':'未成年'}}</h1>
    <!--2.  v-baind: 属性名=“变量” 简写  ： 属性名=“变量”-->
    <a :href="address">百度</a>
    <br>
    <img :src="imgUrl">
    <!--3.  v-on : 事件名=“事件处理”  简写  @事件名=“事件处理” -->
   <h1>{{count}}</h1>
   <button @click="count++">+1</button>
   <button @click="addFn(10)">+10</button>
    <!-- 4. 事件对象 传值 手动添加 $event -->
    <br>
     <a :href="address" @click="addressFn(1,$event)">百度</a>
    <!-- 5. v-on事件修饰符  .stop  阻止冒泡   .prevent 阻止默认事件  .once 事件函数只处理一次-->
    <div @click="fatherFn">
      <span @click.stop="fn1">.stop</span>
      <br>
       <a :href="address" @click.prevent>百度</a>
       <br>
       <span @click.once="onceFn"> .once</span>
    </div>
    <!-- 6. v-on按键修饰符  .enter 回车   .esc 退出 -->
    <input type="text" @keydown.enter="enterFn">
    <input type="text" @keydown.esc="escFn">
    
  </div>
</template>

<script>
import imgUrl from './assets/logo.png'
export default {
 data(){
  return { 
    msg: 'Hello',
    obj:{
      name: 'haa',
      age: 18
    },
    address: 'http://www.baidu.com',
    imgUrl:imgUrl,
    count:0
  }
 },
 methods:{
  addFn(n){
    this.count += n
  },
  addressFn(n,e){
    e.preventDefault()
  },
  fatherFn(){
    console.log('father');
  },
  fn1(){
    console.log('span click');
  },
  onceFn(){
    console.log('once');
  },
  enterFn(){
    alert(1)
  },
  escFn(){
    alert(2)
  }
 }
}
</script>

<style>

</style>