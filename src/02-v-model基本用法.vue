<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-29 02:33:45
 * @LastEditors: sj
 * @LastEditTime: 2022-06-29 02:33:46
-->
<template>
  <div>
     <!-- 	v-model:是实现vuejs 变量和表单标签value属性, 双向绑定的指令-->
     <!-- input  -->
        <div>
      <span>用户名:</span>
      <input type="text" v-model.number="username" />
    </div>
    <div>
      <span>密码:</span>
      <input type="password" v-model.trim="pass" />
    </div>
    <!-- 下拉菜单 -->
     <div>
      <span>来自于: </span>
      <!-- 下拉菜单要绑定在select上 -->
      <select v-model="from">
        <option value="北京市">北京</option>
        <option value="南京市">南京</option>
        <option value="天津市">天津</option>
      </select>
    </div>
    <!-- checkbox 复选框 -->
     <div>
      <!-- (重要)
      遇到复选框, v-model的变量值
      非数组 - 关联的是复选框的checked属性
      数组   - 关联的是复选框的value属性
       -->
      <span>爱好: </span>
      <input type="checkbox" v-model="hobby" value="抽烟">抽烟
      <input type="checkbox" v-model="hobby" value="喝酒">喝酒
      <input type="checkbox" v-model="hobby" value="写代码">写代码
    </div>
     <div>
      <span>爱好: </span>
      <input type="checkbox" v-model="hobby11" value="抽烟">抽烟
      <input type="checkbox" v-model="hobby11" value="喝酒">喝酒
      <input type="checkbox" v-model="hobby11" value="写代码">写代码
    </div>
    <!-- radio 单选按钮 -->
    <div>
      <span>性别: </span>
      <input type="radio" value="男" name="sex" v-model="gender">男
      <input type="radio" value="女" name="sex" v-model="gender">女
    </div>
     <div>
      <span>自我介绍</span>
      <textarea v-model.lazy="intro"></textarea>
    </div>
  </div>

</template>

<script>
export default {
  data(){
   return {
     username: '',
     pass: '',
     from:'',
     hobby:[],
     hobby11:'',
     gender: '',
     intro: '',
   }
  }

}
</script>

<style>

</style>