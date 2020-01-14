<template>
  <el-container>
    <el-aside width="200px">
      <ManualMenu />
    </el-aside>
    <el-main class="main">
      <h1 class="title">团队和项目</h1>
      <el-divider content-position="left">团队与项目列表</el-divider>
      <el-row :gutter="20">
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              点击导航栏“配置管理/项目配置”进入团队与项目列表页。
            </el-timeline-item>
          </el-timeline>
        </el-col>
        <el-col :span="12">
          <el-image :src="step1.src" :alt="step1.alt" />
        </el-col>
      </el-row>
      <el-divider content-position="left">创建团队与项目</el-divider>
      <el-row :gutter="20">
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              点击“创建项目”或“添加”按钮弹出创建项目对话框，填写团队与项目信息，点击“确定”。
            </el-timeline-item>
          </el-timeline>
        </el-col>
        <el-col :span="12">
          <el-image :src="step2.src" :alt="step2.alt" />
        </el-col>
      </el-row>
      <el-divider content-position="left">更新团队与项目</el-divider>
      <el-row :gutter="20">
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              点击“更新”按钮弹出对话框，修改团队与项目信息，点击“确定”。
            </el-timeline-item>
          </el-timeline>
        </el-col>
        <el-col :span="12">
          <el-image :src="step3.src" :alt="step3.alt" />
        </el-col>
      </el-row>
      <el-divider content-position="left">删除团队与项目</el-divider>
      <el-row :gutter="20">
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              点击“删除”按钮弹出对话框，点击“确定”删除团队与项目信息，点击“取消”放弃删除。
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
        src: require("@/assets/img/manual-environment-list.jpg"),
        alt: "manual-environment-list.jpg"
      },
      step2: {
        src: require("@/assets/img/manual-environment-create.jpg"),
        alt: "manual-environment-create.jpg"
      },
      step3: {
        src: require("@/assets/img/manual-environment-update.jpg"),
        alt: "manual-environment-update.jpg"
      },
      step4: {
        src: require("@/assets/img/manual-environment-delete.jpg"),
        alt: "manual-environment-delete.jpg"
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
