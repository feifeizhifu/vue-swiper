<template>
  <div class="home">
    <swiper :options="swiperOption" ref="mySwiper">
      <swiper-slide>
        <img src="http://dummyimage.com/100x50/red" alt />
      </swiper-slide>
      <swiper-slide>
        <img src="http://dummyimage.com/100x50/ff0f0f" alt />
      </swiper-slide>
      <swiper-slide>
        <img src="http://dummyimage.com/100x50/234bca" alt />
      </swiper-slide>
    </swiper>
    <div class="nav">
      <div class="item" v-for="(item,index) in data" :key="index">
        <img :src="item.pic" alt />
        <p>{{item.title}}</p>
      </div>
    </div>
  </div>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper";

export default {
  name: "home",
  data() {
    return {
      data: [
        {
          pic: "http://dummyimage.com/100x100",
          title: "仍无法为"
        },
        {
          pic: "http://dummyimage.com/100x100",
          title: "阿斯蒂芬"
        },
        {
          pic: "http://dummyimage.com/100x100",
          title: "认同与居"
        },
        {
          pic: "http://dummyimage.com/100x100",
          title: "热胎宝宝"
        },
        {
          pic: "http://dummyimage.com/100x100",
          title: "突然有机"
        },
        {
          pic: "http://dummyimage.com/100x100",
          title: "王企鹅服"
        },
        {
          pic: "http://dummyimage.com/100x100",
          title: "的无尽的"
        },
        {
          pic: "http://dummyimage.com/100x100",
          title: "其威锋网"
        }
      ],
      swiperOption: {
        autoplay: true
      }
    };
  },
  computed: {
    swiper() {
      return this.$refs.mySwiper.swiper;
    }
  },
  components: {
    swiper,
    swiperSlide
  }
};
</script>
<style lang="scss">
img {
  width: 100%;
}
.nav{
  display: flex;
  flex-wrap: wrap;
  .item{
    width: 25%;
    text-align: center;
    padding: 10px 0;
    img{
      width: 60%;
      border-radius:50%;
    }
  }
}
</style>
