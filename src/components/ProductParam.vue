<template>
  <div class="nav-bar" :class="{'is-fixed':isFixed}">
    <div class="container">
      <div class="pro-title">{{title}}</div>
      <div class="pro-param">
        <a href="javascript:;">概述</a>
        <span>|</span>
        <a href="javascript:;">参数</a>
        <span>|</span>
        <a href="javascript:;">用户评价</a>
        <slot name="buy"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "nav-bar",
  props: {
    title: String
  },
  data() {
    return {
      isFixed: false
    };
  },
  mounted() {
    window.addEventListener("scroll", this.initHeight);
  },
  methods: {
    initHeight() {
      let scrollTop =
        document.body.scrollTop ||
        window.pageYOffset ||
        document.documentElement.scrollTop;
      this.isFixed = scrollTop > 152;
    }
  },
  destroyed(){
      window.removeEventListener('scroll',this.initHeight,false)
  }
};
</script>
<style lang="scss">
@import "../assets/scss/config.scss";
@import "../assets/scss/mixin.scss";
.nav-bar {
  height: 70px;
  line-height: 70px;
  border-top: 1px solid $colorH;
  z-index: 11;
  &.is-fixed {
    width: 100%;
    position: fixed;
    top: 0;
    background-color: #ffffff;
    box-shadow: 0 5px 5px $colorE;
  }
  .container {
    @include flex();
    .pro-title {
      font-size: $fontH;
      color: $colorB;
      font-weight: bold;
    }
    .pro-param {
      font-size: $fontJ;
      a {
        color: $colorC;
      }
      span {
        margin: 0 10px;
      }
    }
  }
}
</style>