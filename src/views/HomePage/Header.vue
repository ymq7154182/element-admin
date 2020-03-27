<template>
  <div class="header">
    <el-row type="flex" justify="center">
      <el-col :span="4">
        <el-button type="text" class="go-home" @click="gotoHomePage">
          <i class="iconfont icondangwugongkai"></i><span>智慧党建</span>
        </el-button>
      </el-col>
      <el-col :span="2"><el-button type="text">新闻资讯</el-button></el-col>
      <el-col :span="2"><el-button type="text">政策文件</el-button></el-col>
      <el-col :span="2"><el-button type="text">工作动态</el-button></el-col>
      <el-col :span="2"><el-button type="text">党建事务</el-button></el-col>
      <el-col :span="2"><el-button type="text">在线学习</el-button></el-col>
      <el-col :span="2"><el-button type="text">大数据平台</el-button></el-col>
      <el-col :span="2"><el-button type="text" @click="gotoLogin">后台登录</el-button></el-col>
    </el-row>
  </div>
</template>

<script>
    export default {
      name: "Header",
      methods: {
        gotoHomePage() {
          this.$router.push('/')
        },
        gotoLogin () {
          this.$router.push('/login')
        }
      }
    }
</script>

<style scoped>
  .header {
    height: 60px;
    background-color: black;
    color: white;
    text-align: center;
  }

  .el-button {
    color: white;
    margin-top: 11px;
  }

  .el-button:hover {
    color: lightgray;
  }

  .go-home {
    margin: 0;
    font-size: 25px;
  }

  .go-home:hover {
    color: white;
  }

  .go-home i {
    color: red;
    font-size: 30px;
  }

</style>
