<template>
  <el-row class="tac">
    <el-col :span="24">
      <el-menu
        default-active="2"
        class="el-menu-vertical-demo"
        @open="handleOpen"
        @close="handleClose"
      >
        <el-submenu index="1">
          <template slot="title">
            <i class="el-icon-location"></i>
            <span>用户手册</span>
          </template>
          <el-menu-item-group>
            <template slot="title">快速上手</template>
            <el-menu-item index="1-1">linux部署</el-menu-item>
            <el-menu-item index="1-2">docker部署</el-menu-item>
          </el-menu-item-group>
          <el-submenu index="1-3">
            <template slot="title">配置管理</template>
            <el-menu-item index="1-3-1">创建项目与团队</el-menu-item>
            <el-menu-item index="1-3-2">创建全局变量</el-menu-item>
            <el-menu-item index="1-3-3">创建全局关键字</el-menu-item>
          </el-submenu>
          <el-submenu index="1-4">
            <template slot="title">接口管理</template>
            <el-menu-item index="1-4-1">选项1</el-menu-item>
          </el-submenu>
          <el-submenu index="1-5">
            <template slot="title">套件管理</template>
            <el-menu-item index="1-5-1">选项1</el-menu-item>
          </el-submenu>
          <el-menu-item-group title="常见问题">
            <el-menu-item index="1-6">常见问题</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-menu-item index="2">
          <i class="el-icon-menu"></i>
          <span slot="title">python基础</span>
        </el-menu-item>
        <el-menu-item index="3">
          <i class="el-icon-document"></i>
          <span slot="title">接口测试</span>
        </el-menu-item>
        <el-menu-item index="4">
          <i class="el-icon-setting"></i>
          <span slot="title">UI自动化</span>
        </el-menu-item>
      </el-menu>
    </el-col>
  </el-row>
</template>

<script>
export default {
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>
