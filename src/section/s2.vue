<template>
  <section class="s2 user-n w-full relative">
    <img class="logo absolute" src="@/section/s2/logo.svg" />
    <div class="line absolute" data-aos="cuscus" data-aos-delay="0"></div>
    <img class="small absolute" src="@/section/s2/small.webp" />
    <div data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0">
      <div class="t1">夢が示す方向へ<br class="md:hidden">自信を持って進め</div>
      <div class="t2">
        地樺機構｜碩樺建設<br>
        建築生活藝術家
      </div>
    </div>
    <div class="relative md:flex md:items-center md:justify-end md:flex-row-reverse">
      <div class="t3" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0">
        地樺機構深耕房產逾44年，致力推動城市美學，
        以訂製學的心意琢磨建築藝術。建築作品橫跨大型都更案、精品酒店與高端住宅。
        <ol>
          <li><div>中正區 臺北時代寓所‧北投區 天母常玉</div></li>
          <li><div>士林區 天母靜好‧信義區 璞真永吉‧南港區 忠孝無極</div></li>
        </ol>
      </div>
      <div class="slider">
        <swiper
          :loop="true"
          :navigation="true"
          :pagination="{
            clickable: true
          }"
          :autoplay="{
            delay: 3000,
            disableOnInteraction: false,
          }"
          :modules="modules"
        >
          <swiper-slide>
            <div class="img relative">
              <img class="w-full" src="@/section/s2/1.webp" />
              <div class="txt absolute">中正區 臺北時代寓所</div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="img relative">
              <img class="w-full" src="@/section/s2/2.webp" />
              <div class="txt absolute">信義區 璞真永吉</div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="img relative">
              <img class="w-full" src="@/section/s2/3.webp" />
              <div class="txt absolute">北投區 天母常玉</div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="img relative">
              <img class="w-full" src="@/section/s2/4.webp" />
              <div class="txt absolute">南港區 忠孝無極</div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="img relative">
              <img class="w-full" src="@/section/s2/5.webp" />
              <div class="txt absolute">士林區 天母靜好</div>
            </div>
          </swiper-slide>
        </swiper>
      </div>
      <!-- <div class="img relative">
        <img class="w-full" src="@/section/s2/img.webp" />
        <div class="txt absolute">中正區 臺北時代寓所</div>
      </div> -->
    </div>
  </section>
</template>

<style lang="scss">
@import "@/assets/style/function.scss";

[data-aos=cuscus] {
  transform: scaleY(0);
  transition-property: transform;

  &.aos-animate {
    transform: scaleY(1);
  }
}

.s2 {
  background-image: url(@/section/s2/bg.webp);
  background-size: auto size-m(365);
  background-repeat: no-repeat;
  padding-top: size-m(124);
  @media (min-width: 768px) {
    background-size: auto size(1137);
    padding-top: size(278);
  }

  .logo {
    top: size-m(22);
    left: size-m(25);
    width: size-m(48.24);
    @media (min-width: 768px) {
      top: size(82);
      left: size(79);
      width: size(85.38);
    }
  }

  .line {
    top: size-m(106);
    left: size-m(31);
    width: 1px;
    height: calc(100% - size-m(106) - size-m(304));
    background: #C9A063;
    transform-origin: 0 0;
    transition-duration: 2s !important;
    @media (min-width: 768px) {
      top: size(82);
      left: size(242);
      width: size(1);
      height: calc(100% - size(82) - size(716));
    }
  }

  .small {
    top: size-m(29);
    right: 0;
    width: size-m(80);
    @media (min-width: 768px) {
      top: size(82);
      right: 0;
      width: size(273);
    }
  }

  .t1 {
    color: #981F23;
    font-family: "Noto Sans JP";
    font-size: size-m(19);
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    letter-spacing: size-m(3.61);
    margin-bottom: size-m(60);
    padding-left: size-m(55);
    @media (min-width: 768px) {
      font-size: size(51);
      letter-spacing: size(3.57);
      margin-bottom: size(40);
      padding-left: size(398);
    }
  }

  .t2 {
    font-size: size-m(23);
    font-weight: 500;
    line-height: normal;
    letter-spacing: size-m(1.38);
    margin-bottom: size-m(21);
    padding-left: size-m(55);
    @media (min-width: 768px) {
      font-size: size(67);
      letter-spacing: size(0);
      margin-bottom: size(143);
      padding-left: size(398);
    }
  }

  .t3 {
    font-family: "Noto Sans JP";
    font-size: size-m(12);
    font-weight: 500;
    line-height: 173.6%;
    letter-spacing: size-m(0.48);
    margin-bottom: size-m(50);
    padding-left: size-m(55);
    width: size-m(288 + 55);
    @media (min-width: 768px) {
      font-size: size(26);
      font-weight: 500;
      line-height: 163.6%;
      letter-spacing: size(0.52);
      margin-bottom: size(0);
      padding-left: size(112);
      width: size(700);
    }

    ol {
      margin: size-m(24) 0 0 0;
      padding-left: size-m(19);
      color: #981F23;
      font-family: "Noto Sans JP";
      font-size: size-m(11);
      font-style: normal;
      letter-spacing: size-m(0.22);
      list-style: outside;
      @media (min-width: 768px) {
        margin: size(50) 0 0 0;
        padding-left: size(24);
        font-size: size(18);
        letter-spacing: size(0.46);
      }

      div {
        color: #000;
        font-size: size-m(11);
        line-height: 163.6%;
        font-weight: 500;
        @media (min-width: 768px) {
          font-size: size(23);
        }
      }
    }
  }

  .slider {
    @media (min-width: 768px) {
      width: size(1017);
    }

    .swiper-pagination {
      width: auto;
      line-height: 1;
      margin: 0;
      bottom: size-m(13.67);
      padding-left: size-m(17 - 2.92);
      @media (min-width: 768px) {
        bottom: size(32.7);
        padding-left: size(36 - 7.915);
      }

      .swiper-pagination-bullet {
        width: size-m(3.43);
        height: size-m(3.43);
        background: #fff;
        opacity: 1;
        margin: 0 size-m(2.92);
        @media (min-width: 768px) {
          width: size(9.3);
          height: size(9.3);
          margin: 0 size(7.915);
        }

        &.swiper-pagination-bullet-active {
          background: #C30D23;
        }
      }
    }

    .swiper-button-prev, .swiper-button-next {
      width: size-m(5.73);
      height: size-m(16.45);
      background-size: contain;
      @media (min-width: 768px) {
        display: none;
      }

      &::after {
        display: none;
      }
    }

    .swiper-button-prev {
      background-image: url(@/section/s2/arrow-prev.svg);
    }

    .swiper-button-next {
      background-image: url(@/section/s2/arrow-next.svg);
    }
  }

  .img {
    img {
      width: 100%;
      height: size-m(304);
      object-fit: cover;
      @media (min-width: 768px) {
        width: size(1017);
        height: auto;
      }
    }

    .txt {
      bottom: size-m(14);
      right: size-m(16);
      color: #FFF;
      font-family: "Noto Sans JP";
      font-size: size-m(11);
      font-weight: 500;
      line-height: 163.6%;
      letter-spacing: size-m(0.22);
      @media (min-width: 768px) {
        bottom: size(33);
        right: size(49);
        font-size: size(24);
        letter-spacing: size(0.48);
      }
    }
  }
}
</style>

<script setup>
import { ref } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import { Autoplay, Navigation, Pagination } from "swiper";
const modules = ref([Autoplay, Navigation, Pagination]);
</script>
