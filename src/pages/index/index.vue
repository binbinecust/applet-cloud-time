<template>
  <div>
    <swiper
      autoplay
      :interval="3000"
      indicator-dots
    >
      <swiper-item
        v-for="(img, index) in imgs"
        :key="index"
      >
        <div>
          <img
            :src="img"
            alt=""
          >
        </div>
      </swiper-item>
    </swiper>
    <div class="nav-wrapper">
      <div
        v-for="(item, index) in config"
        :key="index"
        @click="toPage(item)"
        class="item"
      >
        <img
          :src="item.url"
          alt=""
        >
        <p>{{item.txt}}</p>
      </div>
    </div>
  </div>
</template>

<script>
import config from './config.js';
export default {
  data() {
    return {
      imgs: [
        'https://www.bibidaodao.cn/assets/album/h5k17itt1vr.jpeg',
        'https://www.bibidaodao.cn/assets/album/ntb2vvj5nsg.jpeg',
        'https://www.bibidaodao.cn/assets/album/afo3tjtla0q.jpeg'
      ],
      config: config
    };
  },
  methods: {
    toPage(item) {
      wx.navigateTo({
        url: item.to
      });
    }
  }
};
</script>

<style lang="scss" scoped>
swiper {
  height: 210px;
  div {
    width: 100%;
    height: 100%;
  }
  img {
    height: 100%;
    width: 100%;
  }
  swiper-item {
    height: 100%;
  }
}

.nav-wrapper {
  padding: 10px;
  display: flex;
  justify-content: space-between;
  text-align: center;
  .item {
    flex: 1;
    font-size: 12px;
    color: #6d6d73;
    img {
      width: 40px;
      height: 40px;
      margin-bottom: 5px;
    }
  }
}
</style>
