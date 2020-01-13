<template>
  <el-row :gutter="20">
    <el-col :span="8" v-for="card in cards" :key="card.alt">
      <el-card :body-style="{ padding: '0px' }">
        <img :src="card.src" class="image">
        <div style="padding: 14px; text-align: center">
          <span>{{ card.title }}</span>
        </div>
      </el-card>
    </el-col>
  </el-row>
</template>


<script>
export default {
  data() {
    return {
      cards: [
        {
          src: require('assets/img/wechat.jpg'),
          alt: 'wechat.jpg',
          title: '大猫聊测试-微信公众号',
          description: 'python与测试技术分享，免费测试技术视频。'
        },
        {
          src: require('assets/img/toutiao.jpg'),
          alt: 'toutiao.jpg',
          title: '大猫聊测试-头条号',
          description: 'python与测试技术分享，免费测试技术视频。'
        },
        {
          src: require('assets/img/qqqun.jpg'),
          alt: 'qqqun.jpg',
          title: 'clover-QQ交流群',
          description: 'clover测试平台交流群，功能与缺陷交流。'
        }
      ],
      currentDate: new Date()
    };
  }
}
</script>

<style>
.tag {
  font-size: 13px;
  color: #999;
  float: left;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
}

.image {
  width: 100%;
  display: block;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}

.clearfix:after {
  clear: both
}
</style>
