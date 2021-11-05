<template>
  <div class="main_box">
    <div class="main">
      <p>Login Page</p>
      <el-input v-model="username" placeholder="请输账号"></el-input>
      <el-input
        placeholder="请输入密码"
        v-model="password"
        show-password
      ></el-input>
      <el-button type="primary" @click="login">登录</el-button>
      <div class="copyright"><u>Copyright © 2021-2021 WUDAO</u></div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      username: "qhl",
      password: "qhl",
    };
  },
  methods: {
    login() {
      axios
        .get("http://81.70.194.181:8089/oauth/token", {
          params: {
            username: this.username,
            password: this.password,
            grant_type: "password",
            client_id: "yutong",
            client_secret: "yutong",
          },
        })
        .then((response) => {
          if (response.status == 200) {
            console.log(response.data);
            this.$router.push({ path: "/home" });
          } else {
            console.log(response.data);
            alert(response.data);
          }
        })
        .catch((error) => {
          alert(error);
          console.log(error);
        });
    },
  },
};
</script>

<style>
body {
  margin: 0px;
}
.main_box {
  display: flex;
  height: 100%vh;
  background-image: url("https://img0.baidu.com/it/u=3690290911,1948613514&fm=26&fmt=auto");
  padding-top: 10%;
  padding-bottom: 15.6%;
}
.main {
  align-items: center;
  width: 400px;
  height: 400px;
  margin: 0 auto;
  background-color: whitesmoke;
  padding: 40px 20px;
  box-shadow: 5px 5px 5px #a8a7a7;
  border-radius: 2%;
}
.main p {
  font-size: 30px;
  margin-top: 20px;
}
.main .el-input {
  width: 300px;
  margin-bottom: 20px;
}
.el-button {
  width: 300px;
}
.copyright {
  padding: 25px;
}
</style>