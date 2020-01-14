<template>
  <el-container>
    <el-aside width="200px">
      <ManualMenu />
    </el-aside>
    <el-main class="main">
      <h1 class="title">变量管理</h1>
      <el-divider content-position="left">变量列表</el-divider>
      <el-row :gutter="20">
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              点击导航栏“配置管理/变量配置”进入变量列表页，可通过下拉菜单选择团队与负责人进行筛选。
            </el-timeline-item>
          </el-timeline>
        </el-col>
        <el-col :span="12">
          <el-image :src="step1.src" :alt="step1.alt" />
        </el-col>
      </el-row>
      <el-divider content-position="left">创建变量</el-divider>
      <el-row :gutter="20">
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              点击“创建变量”或“添加”按钮弹出创建项目对话框，填写团队、项目、负责人、变量名与变量值，点击“确定”。
            </el-timeline-item>
          </el-timeline>
        </el-col>
        <el-col :span="12">
          <el-image :src="step2.src" :alt="step2.alt" />
        </el-col>
      </el-row>
      <el-divider content-position="left">更新变量</el-divider>
      <el-row :gutter="20">
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              点击“更新”按钮弹出对话框，修改团队、项目、负责人、变量名与变量值，点击“确定”。
            </el-timeline-item>
          </el-timeline>
        </el-col>
        <el-col :span="12">
          <el-image :src="step3.src" :alt="step3.alt" />
        </el-col>
      </el-row>
      <el-divider content-position="left">删除变量</el-divider>
      <el-row :gutter="20">
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              点击“删除”按钮弹出对话框，点击“确定”删除团队、项目、负责人、变量名与变量值，点击“取消”放弃删除。
            </el-timeline-item>
          </el-timeline>
        </el-col>
        <el-col :span="12">
          <el-image :src="step4.src" :alt="step4.alt" />
        </el-col>
      </el-row>
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
        src: require("@/assets/img/manual-variable-list.jpg"),
        alt: "manual-variable-list.jpg"
      },
      step2: {
        src: require("@/assets/img/manual-variable-create.jpg"),
        alt: "manual-variable-create.jpg"
      },
      step3: {
        src: require("@/assets/img/manual-variable-update.jpg"),
        alt: "manual-variable-update.jpg"
      },
      step4: {
        src: require("@/assets/img/manual-variable-delete.jpg"),
        alt: "manual-variable-delete.jpg"
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

.title {
  padding-bottom: 20px;
  font-size: 36px;
}

.timeline {
  padding-top: 20px;
}
</style>
