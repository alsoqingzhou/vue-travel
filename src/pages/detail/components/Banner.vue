<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img
        class="banner-img"
        src="http://img1.qunarzz.com/sight/p0/1507/cc/19733fc0135062788140cbb48ae606a7.water.jpg_350x240_05ea2c18.jpg"
      />
      <div class="banner-info">
        <div class="banner-title">北京野生动物园(AAAA景区)</div>
        <div class="banner-num">
          <span class="iconfont banner-icon">&#xe635;</span>
          35
        </div>
      </div>
    </div>
    <common-gallary
        :imgs="imgs"
        v-show="showGallary"
        @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/2002/f6/f60df9dd1ce24076a3.img.jpg_350x240_4232328e.jpg',
        'http://img1.qunarzz.com/sight/p39/201211/05/0253fe2d21086d9f93835fbb.jpg_350x240_8f00b658.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
.banner {
  position: relative;
  overflow: hidden;
  height: 0;
  padding-bottom: 68.57%;

  .banner-img {
    width: 100%;
  }

  .banner-info {
    display: flex;
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    line-height: 0.6rem;
    color: #ffffff;
    background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8));

    .banner-title {
      flex: 1;
      font-size: 0.32rem;
      padding: 0 0.2rem;
    }

    .banner-num {
      padding: 0 0.4rem;
      height: 0.32rem;
      margin-top: 0.14rem;
      line-height: 0.32rem;
      border-radius: 0.2rem;
      background: rgba(0, 0, 0, 0.8);
      font-size: 0.24rem;

      .banner-icon {
        font-size: 0.24rem;
      }
    }
  }
}
</style>
