<template>
  <div>
    <h2>功能介绍</h2>
    <div class="content">
      <el-row :gutter="36">
        <el-col :span="8" v-for="card in cards" :key="card.alt">
          <el-card :body-style="{ padding: '0px' }">
            <img :src="card.src" class="image" />
            <div style="padding: 14px;">
              <p class="headline">{{ card.title }}</p>
              <p class="description">{{ card.description }}</p>
            </div>
          </el-card>
        </el-col>
      </el-row>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          src: require("assets/img/introduce-01.jpg"),
          alt: "python",
          title: "功能完备",
          description: "hook机制、fixture特性应有尽有，支持正则与分隔符两种断言方法，用例可以自由组合为套件，支持按照套件运行。"
        },
        {
          src: require("assets/img/introduce-02.jpg"),
          alt: "flask",
          title: "资料丰富",
          description: "clover平台有丰富的文档和视频教程，当您使用遇到问题时可以通过文档和视频查找解决方案，也可以直接和开发者交流。"
        },
        {
          src: require("assets/img/introduce-03.jpg"),
          alt: "jenkins",
          title: "注重体验",
          description: "每一个细节都是我们改进的发力点，您使用的过程中有好的体验改进建议可以直接提issue，开发者讨论通过后就会排期优化。"
        }
      ]
    };
  }
};
</script>

<style scoped>
h2 {
  font-size: 38px;
  line-height: 46px;
  color: #0d1a26;
  font-weight: 400;
  margin-bottom: 32px;
}

.content {
  margin-left: 66px;
  margin-right: 66px;
  padding-top: 36px;
  padding-left: 24px;
  padding-right: 24px;
}

.image {
  width: 100%;
  display: block;
}

.headline {
  color: #0d1a26;
  font-size: 20px;
  margin: 8px auto;
}

.description {
  text-decoration: none;
  color: #5e6e7d;
  font-size: 14px;
  text-align: left;
  font-family: Arial, Helvetica, sans-serif;
  width: 90%;
  display: inline-block;
  will-change: transform;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}

.clearfix:after {
  clear: both;
}
</style>
