<template>
  <el-container>
    <el-aside width="200px">
      <ManualMenu />
    </el-aside>
    <el-main class="main">
      <h1 class="title">使用docker部署</h1>
      <el-alert
        title="请先安装docker与mysql，mysql版本应大于等于5.7！"
        type="error"
        close-text="朕知道了"
      >
      </el-alert>
      <el-divider content-position="left">第一步</el-divider>
      <el-row align="middle">
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              create database if not exists clover;
            </el-timeline-item>
            <el-timeline-item>
              create user "clover"@"%" identified by "52.clover";
            </el-timeline-item>
            <el-timeline-item>
              grant all privileges on clover.* to 'clover'@'%';
            </el-timeline-item>
            <el-timeline-item>
              flush privileges;
            </el-timeline-item>
          </el-timeline>
        </el-col>
        <el-col :span="12">
          <el-image :src="step1.src" :alt="step1.alt" />
        </el-col>
      </el-row>
      <el-divider content-position="left">第二步</el-divider>
      <el-row>
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              'host': '127.0.0.1'改为'host': '{your mysql ip}'
            </el-timeline-item>
          </el-timeline>
        </el-col>
        <el-col :span="12">
          <el-image :src="step2.src" :alt="step2.alt" />
        </el-col>
      </el-row>
      <el-divider content-position="left">第三步</el-divider>
      <el-row>
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              "generate": "cross-env BASE_URL=http://{docker ip}:8080
              NODE_ENV=production nuxt
            </el-timeline-item>
          </el-timeline>
        </el-col>
        <el-col :span="12">
          <el-image :src="step3.src" :alt="step3.alt" />
        </el-col>
      </el-row>
      <el-divider content-position="left">第四步</el-divider>
      <el-row>
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              docker build -f Dockerfile .
            </el-timeline-item>
            <el-timeline-item>
              docker images
            </el-timeline-item>
            <el-timeline-item>
              docker run -itd -p 8080:8080 {image_id}
            </el-timeline-item>
          </el-timeline>
        </el-col>
        <el-col :span="12">
          <el-image :src="step4.src" :alt="step4.alt" />
        </el-col>
      </el-row>
      <el-divider content-position="left">第五步</el-divider>
      <el-row>
        <el-col :span="12">
          <el-timeline class="timeline">
            <el-timeline-item>
              打开浏览器输入http://{docker ip}:8080访问平台
            </el-timeline-item>
          </el-timeline>
        </el-col>
        <el-col :span="12">
          <el-image :src="step5.src" :alt="step5.alt" />
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
        src: require("@/assets/img/manual-mysql-init.jpg"),
        alt: "manual-mysql-init.jpg"
      },
      step2: {
        src: require("@/assets/img/manual-mysql-ip.jpg"),
        alt: "manual-mysql-ip.jpg"
      },
      step3: {
        src: require("@/assets/img/manual-docker-ip.jpg"),
        alt: "manual-docker-ip.jpg"
      },
      step4: {
        src: require("@/assets/img/manual-docker-cmd.jpg"),
        alt: "manual-docker-cmd.jpg"
      },
      step5: {
        src: require("@/assets/img/manual-clover-index.jpg"),
        alt: "manual-clover-index.jpg"
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
