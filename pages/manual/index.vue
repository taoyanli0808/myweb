<template>
  <el-container>
    <el-aside width="200px">
      <ManualMenu />
    </el-aside>
    <el-main>Main</el-main>
  </el-container>
</template>

<script>
import ManualMenu from "~/components/ManualMenu.vue";

export default {
  components: {
    ManualMenu
  }
};
</script>
