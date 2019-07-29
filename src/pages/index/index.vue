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
    <van-button></van-button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgs: [
        'https://www.bibidaodao.cn/assets/album/h5k17itt1vr.jpeg',
        'https://www.bibidaodao.cn/assets/album/ntb2vvj5nsg.jpeg',
        'https://www.bibidaodao.cn/assets/album/afo3tjtla0q.jpeg'
      ]
    };
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
</style>
