<template>
  <el-menu
    :default-active="activeIndex"
    class="el-menu-demo"
    mode="horizontal"
  >
    <el-menu-item index="1">
      <a href="/">首页</a>
    </el-menu-item>
    <el-menu-item index="2">
      <a href="/manual">用户手册</a>
    </el-menu-item>
    <el-menu-item index="3">
      <a href="/trial">快速体验</a>
    </el-menu-item>
    <el-menu-item index="4">
      <a href="/about">关于clover</a>
    </el-menu-item>
  </el-menu>
</template>

<script>
export default {
  data () {
    return {
      activeIndex: '1',
      activeIndex2: '1'
    }
  }
}
</script>
