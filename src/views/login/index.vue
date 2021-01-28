<template>
  <div class="login-container">
    <div class="login-box">
      <h2 style="text-align: center">Admin</h2>
      <el-form ref="loginFormRef"
               :model="loginForm">
        <el-form-item>
          <el-input v-model="loginForm.username" placeholder="请输入用户名"
                    prefix-icon="iconfont iconuser"></el-input>
        </el-form-item>
        <el-form-item>
          <el-input v-model="loginForm.password" placeholder="请输入密码"
                    prefix-icon="iconfont iconpassword"></el-input>
        </el-form-item>
        <el-form-item class="btn">
          <el-button type="primary"
                     @click="onLogin">登录</el-button>
          <el-button>重置</el-button>
        </el-form-item>
      </el-form>
    </div>

  </div>
</template>

<script>
export default {
  name: 'login',
  components: {},
  props: {},
  data () {
    return {
      loginForm: {
        username: '',
        password: ''
      }
    }
  },
  computed: {},
  watch: {},
  created () { },
  mounted () { },
  methods: {
    onLogin () {
      console.log('submit!')
    }
  }
}
</script>

<style scoped lang="less">
.login-container {
  width: 100%;
  height: 100%;
  // display: flex;
  // justify-content: center;
  // align-items: center;
  background: url("./login_bg.jpg") no-repeat;
  background-size: cover;
}
.login-box {
  width: 450px;
  height: 250px;
  background-color: #fff;
  border-radius: 5px;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  .el-form {
    position: absolute;
    bottom: 0;
    width: 100%;
    padding: 0 20px;
    box-sizing: border-box;
  }
  .btn {
    display: flex;
    justify-content: flex-end;
  }
}
</style>
