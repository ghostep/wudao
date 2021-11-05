<template>
  <div class="home">
    <el-container>
      <el-container>
        <el-header>
          <el-input
            class="search-input"
            v-model="content"
            placeholder="请输入内容"
          ></el-input>
          <el-button
            class="search-button"
            icon="el-icon-search"
            circle
          ></el-button>
          <el-button
            class="edit-button"
            type="primary"
            icon="el-icon-edit"
            circle
          />
          <router-link to="/">
            <el-button
              class="user-button"
              type="sucess"
              icon="el-icon-user"
              circle
            />
          </router-link>
        </el-header>
        <el-main>
          <el-row
            :span="8"
            v-for="(o, index) in 10"
            :key="o"
            :offset="index > 0 ? 25 : 0"
          >
            <el-card :body-style="{ padding: '12px' }">
              <div style="padding: 14px">
                <span
                  >具有工作流动态审批、加签、会签等工作流功能，可以对工作流程的审批业务进行评论/讨论
                  具有文档预览、图片预览等功能
                  具有博客编写、预览、查看、搜索等功能 具有社区、问答等功能
                  具有OA系统常用功能 具有在线网盘等功能
                  工作流引擎完全手写且开源，可以类似钉钉/飞书那样，动态选择审批人员。
                  具有工作流动态审批、加签、会签等工作流功能，可以对工作流程的审批业务进行评论/讨论
                  具有文档预览、图片预览等功能
                  具有博客编写、预览、查看、搜索等功能 具有社区、问答等功能
                  具有OA系统常用功能 具有在线网盘等功能
                  工作流引擎完全手写且开源，可以类似钉钉/飞书那样，动态选择审批人员。
                  具有工作流动态审批、加签、会签等工作流功能，可以对工作流程的审批业务进行评论/讨论
                  具有文档预览、图片预览等功能
                  具有博客编写、预览、查看、搜索等功能 具有社区、问答等功能
                  具有OA系统常用功能 具有在线网盘等功能
                  工作流引擎完全手写且开源，可以类似钉钉/飞书那样，动态选择审批人员。
                  具有工作流动态审批、加签、会签等工作流功能，可以对工作流程的审批业务进行评论/讨论
                  具有文档预览、图片预览等功能
                  具有博客编写、预览、查看、搜索等功能 具有社区、问答等功能
                  具有OA系统常用功能 具有在线网盘等功能
                  工作流引擎完全手写且开源，可以类似钉钉/飞书那样，动态选择审批人员。
                  具有工作流动态审批、加签、会签等工作流功能，可以对工作流程的审批业务进行评论/讨论
                  具有文档预览、图片预览等功能
                  具有博客编写、预览、查看、搜索等功能 具有社区、问答等功能
                  具有OA系统常用功能 具有在线网盘等功能
                  工作流引擎完全手写且开源，可以类似钉钉/飞书那样，动态选择审批人员。
                  具有工作流动态审批、加签、会签等工作流功能，可以对工作流程的审批业务进行评论/讨论
                  具有文档预览、图片预览等功能
                  具有博客编写、预览、查看、搜索等功能 具有社区、问答等功能
                  具有OA系统常用功能 具有在线网盘等功能
                  工作流引擎完全手写且开源，可以类似钉钉/飞书那样，动态选择审批人员。
                </span>
                <div class="bottom clearfix">
                  <time class="time">{{ currentDate }}</time>
                </div>
              </div>
            </el-card>
          </el-row>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  data() {
    return {
      currentDate: new Date(),
      content: "",
    };
  },
  methods: {
    toLogin() {
      console.log("Jfi");
    },
  },
};
</script>

<style>
.user-button {
  max-width: 40px;
}

.el-header {
  background-color: rgb(255, 255, 255);
}
.el-main {
  background-color: rgba(219, 225, 226, 0.603);
  color: #333;
  text-align: center;
  line-height: 20px;
  margin: center;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
.edit-button {
  max-width: 40px;
}
.login-button {
  max-width: 40px;
}
.search-input {
  width: 690px;
}
.search-button {
  max-width: 40px;
}
.time {
  font-size: 13px;
  color: #999;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
}

.button {
  padding: 0;
  float: right;
}

.image {
  width: 100%;
  height: 400px;
  display: block;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}

.clearfix:after {
  clear: both;
}
.el-card {
  max-width: 650px;
  margin: 0 auto;
  padding: 15px;
}
</style>
