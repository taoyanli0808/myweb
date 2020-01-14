<template>
  <div class="container">
    <h2>大记事</h2>
    <el-row class="row">
      <img class="image" :src="timeline" alt="timeline">
    </el-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      timeline: require("assets/img/timeline.jpg"),
    }
  }
};
</script>

<style scoped>
.container {
  margin-left: 66px;
  margin-right: 66px;
  padding-top: 36px;
  padding-left: 24px;
  padding-right: 24px;
}

h2 {
  font-size: 38px;
  line-height: 46px;
  color: #0d1a26;
  font-weight: 400;
  margin-bottom: 32px;
}

.image {
  width: 100%;
  display: block;
  padding-bottom: 36px;
}
</style>
