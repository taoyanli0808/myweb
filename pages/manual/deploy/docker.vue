<template>
  <el-container>
    <el-aside width="200px">
      <ManualMenu />
    </el-aside>
    <el-main class="main">
      <h1>使用docker部署</h1>
      <el-alert
        title="请先安装docker与mysql，mysql版本应大于等于5.7！"
        type="error"
        close-text="朕知道了"
      >
      </el-alert>
      <el-divider content-position="left">第一步</el-divider>
      <el-row>
        <el-col :span="12">
          create database if not exists clover;<br />
          create user "clover"@"%" identified by "52.clover";<br />
          grant all privileges on clover.* to 'clover'@'%';<br />
          flush privileges;<br />
        </el-col>
        <el-col :span="12">
          <el-img class="image" :src="step1.src" :alt="step1.alt"></el-img>
        </el-col>
      </el-row>
      <el-divider content-position="left">第二步</el-divider>
      <el-divider content-position="left">第三步</el-divider>
      <el-divider content-position="left">第四步</el-divider>
      <el-divider content-position="left">第五步</el-divider>
    </el-main>
  </el-container>
</template>

<script>
import ManualMenu from "~/components/ManualMenu.vue";

export default {
  components: {
    ManualMenu
  },
  data() {
    return {
      step1: {
        src: require("assets/img/manual-mysql-init.jpg"),
        alt: "manual-mysql-init.jpg"
      }
    };
  }
};
</script>

<style scoped>
.main {
  padding-left: 36px;
  padding-right: 36px;
}
</style>
