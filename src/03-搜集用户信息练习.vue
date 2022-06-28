<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-29 02:57:16
 * @LastEditors: sj
 * @LastEditTime: 2022-06-29 02:57:17
-->
<template>
  <div>
    <!-- 练习一， 搜集用户信息 -->
    <div>
      <span>选择所在地区</span>：
      <input type="radio" value="中国大陆" name="area" v-model="area" />中国大陆
      <input type="radio" value="中国香港" name="area" v-model="area" />中国香港
    </div>
    <div>
      <span>手机号码</span>：
      <input type="tel" name="phone" v-model.number="phone" />
    </div>
    <div>
      <span>年龄</span>：
      <input type="number" name="age" v-model.number="age" />
    </div>
    <div>
      <span>密码</span>：
      <input type="password" name="pass" v-model="pass" />
    </div>
    <div>
      <span>爱好：</span>
      <input type="checkbox" v-model="hobby" value="看书" />看书
      <input type="checkbox" v-model="hobby" value="学习" />学习
      <input type="checkbox" v-model="hobby" value="写代码" />写代码
      <input type="checkbox" v-model="hobby" value="游戏" />游戏
    </div>
    <div><input type="checkbox" v-model="isgrow" /> 记住密码</div>
    ===============================================
    <div>
      我来自：{{ area}}
      <br />
      手机号码是：{{phone}}
      <br />
      年龄是：{{age}}
      <br />
      密码是：{{pass}}
      <br />
      爱好是：{{hobby}}
      <br />
      是否记住密码：{{ isgrow ? '是' : '否' }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      area: '中国大陆',
      phone: '',
      age: '',
      pass: '',
      hobby:['写代码'],
      isgrow:''
    }
  },
}
</script>

<style></style>
