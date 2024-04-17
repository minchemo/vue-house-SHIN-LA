<template>
  <section class="s7 w-full relative text-[#040000]">
    <div class="t1" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0">全球工藝 品牌精選</div>
    <img class="balls absolute hidden md:block" src="@/section/s7/balls.png" />
    <div class="md:flex md:justify-between md:items-start">
      <img class="img" src="@/section/s7/img.png" />
      <div class="slider md:hidden">
        <swiper
          :loop="true"
          :navigation="false"
          :autoplay="{
            delay: 3000,
            disableOnInteraction: false,
          }"
          :modules="modules"
          @init="init1"
        >
          <swiper-slide>
            <div class="relative">
              <img src="@/section/s7/slider/1.jpg" />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="relative">
              <img src="@/section/s7/slider/2.jpg" />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="relative">
              <img src="@/section/s7/slider/3.jpg" />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="relative">
              <img src="@/section/s7/slider/4.jpg" />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="relative">
              <img src="@/section/s7/slider/5.jpg" />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="relative">
              <img src="@/section/s7/slider/6.jpg" />
            </div>
          </swiper-slide>
        </swiper>

        <div class="slide-prev" @click="slidePrev1">
          <svg viewBox="0 0 32 31" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="15.5" cy="15.5" r="15.5" transform="matrix(-1 0 0 1 31 0)" fill="white"/>
            <path d="M18.7295 24.5416L8.39616 14.8541" stroke="#E5005C" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M18.7295 5.8124L8.39616 14.8541" stroke="#E5005C" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <div class="slide-next" @click="slideNext1">
          <svg viewBox="0 0 32 31" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="15.5" cy="15.5" r="15.5" fill="white"/>
            <path d="M12.2705 24.5416L22.6038 14.8541" stroke="#E5005C" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M12.2705 5.8124L22.6038 14.8541" stroke="#E5005C" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
      </div>
      <div class="slider hidden md:block">
        <swiper
          :loop="true"
          :navigation="false"
          :autoplay="{
            delay: 3000,
            disableOnInteraction: false,
          }"
          :modules="modules"
          @init="init2"
        >
          <swiper-slide>
            <div class="relative">
              <img src="@/section/s7/1.png" />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="relative">
              <img src="@/section/s7/2.png" />
            </div>
          </swiper-slide>
        </swiper>

        <div class="slide-prev" @click="slidePrev2">
          <svg viewBox="0 0 32 31" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="15.5" cy="15.5" r="15.5" transform="matrix(-1 0 0 1 31 0)" fill="white"/>
            <path d="M18.7295 24.5416L8.39616 14.8541" stroke="#E5005C" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M18.7295 5.8124L8.39616 14.8541" stroke="#E5005C" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <div class="slide-next" @click="slideNext2">
          <svg viewBox="0 0 32 31" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="15.5" cy="15.5" r="15.5" fill="white"/>
            <path d="M12.2705 24.5416L22.6038 14.8541" stroke="#E5005C" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M12.2705 5.8124L22.6038 14.8541" stroke="#E5005C" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
@import "@/assets/style/function.scss";

.s7 {
  padding: size-m(24) 0;
  background-image: url(@/section/s7/bg-m.png);
  background-size: cover;
  @media (min-width: 768px) {
    padding: size(90) size(250);
    background: none;
  }

  .t1 {
    font-size: size-m(25);
    line-height: size-m(34);
    color: #E5005C;
    font-weight: 700;
    padding: 0 size-m(30);
    margin-bottom: size-m(20);
    @media (min-width: 768px) {
      font-size: size(58);
      line-height: size(79);
      padding: 0;
      margin-bottom: size(30);
    }
  }

  .balls {
    @media (min-width: 768px) {
      top: size(69);
      left: size(789);
      width: size(276);
    }
  }

  .img {
    position: relative;
    width: size-m(332);
    margin: 0 auto size-m(20) auto;
    @media (min-width: 768px) {
      width: size(1029);
      margin: 0;
    }
  }

  .slider {
    position: relative;
    @media (min-width: 768px) {
      width: size(227);
      padding-top: size(47);
    }

    .swiper {
      width: size-m(231);
      margin: 0 auto;
      @media (min-width: 768px) {
        width: 100%;
      }
    }

    .swiper-slide img {
      display: block;
      width: 100%;
    }

    .slide-prev, .slide-next {
      width: size-m(31);
      cursor: pointer;
      position: absolute;
      top: 50%;
      left: size-m(14);
      transform: translate(0, -50%);
      @media (min-width: 768px) {
        width: size(31);
        top: 0;
        left: 0;
        transform: translate(0, 0);
      }
      
      svg {
        display: block;
        width: 100%;

        @media (min-width: 768px) {
          circle {
            fill: #E5005C;
          }

          path {
            stroke: #fff;
          }
        }
      }
    }

    .slide-next {
      left: auto;
      right: size-m(14);
      @media (min-width: 768px) {
        right: 0;
      }
    }
  }
}
</style>

<script setup>
import { ref } from "vue"
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import 'swiper/css/navigation';
import { Autoplay, Navigation } from "swiper";
const modules = ref([Autoplay, Navigation]);
const swiperRef1 = ref(null);
const swiperRef2 = ref(null);

const init1 = swiper => {
  swiperRef1.value = swiper;
}

const slidePrev1 = () => {
  if(swiperRef1.value){
    swiperRef1.value.slidePrev();
  }
}

const slideNext1 = () => {
  if(swiperRef1.value){
    swiperRef1.value.slideNext();
  }
}

const init2 = swiper => {
  swiperRef2.value = swiper;
}

const slidePrev2 = () => {
  if(swiperRef2.value){
    swiperRef2.value.slidePrev();
  }
}

const slideNext2 = () => {
  if(swiperRef2.value){
    swiperRef2.value.slideNext();
  }
}
</script>