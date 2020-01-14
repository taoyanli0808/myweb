<template>
  <el-container>
    <el-header class="box_fixed" id="boxFixed" :class="{'is_fixed' : isFixed}">
      <Header />
    </el-header>
    <el-main>
      <nuxt />
    </el-main>
    <el-footer>
      <Footer />
    </el-footer>
  </el-container>
</template>

<script>
import Header from './Header.vue'
import Footer from './Footer.vue'

export default {
  components: {
    Header,
    Footer
  },
  data() {
    return {
      isFixed: false,
      offsetTop: 0
    }
  },
  mounted() {
    window.addEventListener('scroll', this.initHeight);
    this.$nextTick(() => {
      //获取对象相对于版面或由 offsetTop 属性指定的父坐标的计算顶端位置
      this.offsetTop = document.querySelector('#boxFixed').offsetTop;
    })
  },
  methods: {
    initHeight() {
      // 设置或获取位于对象最顶端和窗口中可见内容的最顶端之间的距离 (被卷曲的高度)
      var scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop
      //如果被卷曲的高度大于吸顶元素到顶端位置 的距离
      this.isFixed = scrollTop > this.offsetTop ? true : false;
    },
  },
  //回调中移除监听
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

body {
  font-family: -apple-system,BlinkMacSystemFont,Segoe UI,PingFang SC,Hiragino Sans GB,Microsoft YaHei,Helvetica Neue,Helvetica,Arial,sans-serif,Apple Color Emoji,Segoe UI Emoji,Segoe UI Symbol
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.box_fixed {
  width: 100%;
  margin: 0 auto;
  height: 40px;
  line-height: 40px;
}

.is_fixed {
  top: 0;
  position: fixed;
  z-index: 999;
}
</style>
