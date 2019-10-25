<template>
  <div class="box">
<el-card class="box-card">
      <img src="../../assets/logo_index.png" alt="">
<el-form ref="form" :model="loginform">
  <el-form-item>
    <el-input v-model="loginform.name" placeholder="请输入姓名"></el-input>
  </el-form-item>
    <el-form-item>
    <el-input v-model="loginform.code" placeholder="请输入验证码" style="width:238px;margin-right:10px"></el-input>
    <el-button>发送验证码</el-button>
    <el-checkbox :checked="true">同意用户隐私协议</el-checkbox>
  </el-form-item>

  <el-form-item>
    <el-button type="primary" style="width:100%">登录</el-button>
  </el-form-item>
</el-form>
</el-card>
  </div>
</template>

<script>
export default {
  data () {
    return {
      loginform: {
        name: '',
        code: ''
      }
    }
  }

}
</script>

<style scoped lang='less'>
.box{
    width: 100%;
    height: 100%;
    background:url("../../assets/login_bg.jpg") no-repeat center / cover;
    position: absolute;
    left: 0;
    top: 0;
}
.el-card{
    width: 400px;
    height: 340px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%,-50%);
    img {
        display: block;
        margin: 0 auto;
        margin-bottom: 20px;
    }

}
</style>
