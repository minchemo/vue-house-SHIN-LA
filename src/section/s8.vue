<template>
  <section class="s8 w-full relative text-[#040000]">
    <img class="line" src="@/section/s8/line.svg" />
    <img class="balls absolute hidden md:block" src="@/section/s8/balls.webp" />
    <div class="md:flex title" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0">
      <div class="t1">有光有景 寬心大格局</div>
      <div class="t2">光空間，寬格局，逍遙大尺度！明亮舒適的起居空間，讓生活與心情輕快飛揚。</div>
    </div>

    <div class="md:flex md:justify-between md:items-end">
      <div class="slider relative">
        <Transition>
          <div v-if="room === 2">
            <swiper
              :loop="true"
              :navigation="false"
              :pagination="{
                clickable: true,
              }"
              :autoplay="{
                delay: 3000,
                disableOnInteraction: false,
              }"
              :modules="modules"
              @init="init1"
            >
              <swiper-slide>
                <div class="relative">
                  <img src="@/section/s8/2/1.webp" />
                  <div class="txt">實品屋實景</div>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="relative">
                  <img src="@/section/s8/2/2.webp" />
                  <div class="txt">實品屋實景</div>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="relative">
                  <img src="@/section/s8/2/3.webp" />
                  <div class="txt">實品屋實景</div>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="relative">
                  <img src="@/section/s8/2/4.webp" />
                  <div class="txt">實品屋實景</div>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="relative">
                  <img src="@/section/s8/2/5.webp" />
                  <div class="txt">實品屋實景</div>
                </div>
              </swiper-slide>
            </swiper>
            <div class="slide-prev" @click="slidePrev1">
          <svg viewBox="0 0 8 8" fill="#E5005C" xmlns="http://www.w3.org/2000/svg"><circle cx="4" cy="4" r="4"/><path stroke="#FFF" stroke-linecap="round" stroke-linejoin="round" d="M4.8,1.5L2.2,3.8l2.7,2.5"/></svg>
            </div>
            <div class="slide-next" @click="slideNext1">
          <svg viewBox="0 0 8 8" fill="#E5005C" xmlns="http://www.w3.org/2000/svg"><circle cx="4" cy="4" r="4"/><path stroke="#FFF" stroke-linecap="round" stroke-linejoin="round" d="M3.2,6.5l2.7-2.3L3.2,1.7"/></svg>
            </div>
          </div>
          <div v-else>
            <swiper
              :loop="true"
              :navigation="false"
              :pagination="{
                clickable: true,
              }"
              :autoplay="{
                delay: 3000,
                disableOnInteraction: false,
              }"
              :modules="modules"
              @init="init2"
            >
              <swiper-slide>
                <div class="relative">
                  <img src="@/section/s8/3/1.webp" />
                  <div class="txt">實品屋實景</div>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="relative">
                  <img src="@/section/s8/3/2.webp" />
                  <div class="txt">實品屋實景</div>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="relative">
                  <img src="@/section/s8/3/3.webp" />
                  <div class="txt">實品屋實景</div>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="relative">
                  <img src="@/section/s8/3/4.webp" />
                  <div class="txt">實品屋實景</div>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="relative">
                  <img src="@/section/s8/3/5.webp" />
                  <div class="txt">實品屋實景</div>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="relative">
                  <img src="@/section/s8/3/6.webp" />
                  <div class="txt">實品屋實景</div>
                </div>
              </swiper-slide>
            </swiper>
            <div class="slide-prev" @click="slidePrev2">
          <svg viewBox="0 0 8 8" fill="#E5005C" xmlns="http://www.w3.org/2000/svg"><circle cx="4" cy="4" r="4"/><path stroke="#FFF" stroke-linecap="round" stroke-linejoin="round" d="M4.8,1.5L2.2,3.8l2.7,2.5"/></svg>
            </div>
            <div class="slide-next" @click="slideNext2">
          <svg viewBox="0 0 8 8" fill="#E5005C" xmlns="http://www.w3.org/2000/svg"><circle cx="4" cy="4" r="4"/><path stroke="#FFF" stroke-linecap="round" stroke-linejoin="round" d="M3.2,6.5l2.7-2.3L3.2,1.7"/></svg>
            </div>
          </div>
        </Transition>
      </div>
      <div class="content md:flex md:flex-col-reverse">
        <div class="room-btns flex justify-between items-start">
          <div :class="{'room-btn': true, 'active': room === 2}" @click="room = 2"><span>2</span>房</div>
          <div :class="{'room-btn': true, 'active': room === 3}" @click="room = 3"><span>3</span>房</div>
        </div>
        <div data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0">
          <div class="t1">美式輕時尚，經典再造</div>
          <div class="t2">
            規劃完整落塵區，內外區分保持清潔。<br>
            美式STYLE早餐檯，客廳機能多元化。<br>
            無多餘過道，坪效運用優。<br>
            大陽台規劃，面西視野遼闊。<br>
            鄰房皆為透天，5F以上享無限棟距。
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
@import "@/assets/style/function.scss";

.s8 {
  padding: size-m(24) 0;
  background-image: url(@/section/s7/bg-m.png);
  background-size: cover;
  @media (min-width: 768px) {
    padding: size(90) size(250);
    background: none;
  }
  
  .v-enter-active,
  .v-leave-active {
    transition: opacity .4s;
  }

  .v-enter-from,
  .v-leave-to {
    opacity: 0;
  }

  .v-enter-to,
  .v-leave-from {
    opacity: 1;
  }

  .line {
    display: none;
    @media (min-width: 768px) {
      display: block;
      position: absolute;
      top: 0;
      left: 0;
      width: size(1390);
    }
  }

  .balls {
    pointer-events: none;
    @media (min-width: 768px) {
      top: size(-97);
      left: size(1075);
      width: size(646);
    }
  }

  .t1 {
    font-size: size-m(25);
    line-height: size-m(34);
    color: #E5005C;
    font-weight: 700;
    padding: 0 size-m(30);
    margin-bottom: size-m(20);
    @media (min-width: 768px) {
      font-size: size(31);
      line-height: size(42);
      padding: 0;
      margin-bottom: size(19);
    }
  }

  .t2 {
    font-size: size-m(14);
    line-height: 178%;
    color: #040000;
    padding: 0 size-m(30);
    margin-bottom: size-m(13);
    @media (min-width: 768px) {
      font-size: size(18);
      padding: 0;
      margin-bottom: size(93);
    }
  }

  .title {
    @media (min-width: 768px) {
      margin: 0 0 size(32) 0;
      align-items: center;

      .t1 {
        font-size: size(58);
        line-height: size(79);
        margin: 0 size(48) 0 0;
      }

      .t2 {
        margin: 0;
        width: size(405);
      }
    }
  }

  .slider {
    overflow: hidden;
    position: relative;
    height: size-m(210);
    @media (min-width: 768px) {
      width: size(991);
      height: size(660 + 52);
      padding-bottom: size(52);
    }

    .swiper {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      overflow: visible;
    }

    .swiper-slide {
      img {
        display: block;
        width: 100%;
        height: size-m(210);
        object-fit: cover;
        @media (min-width: 768px) {
          height: size(660);
        }
      }

      .txt {
        position: absolute;
        bottom: size-m(6);
        left: size-m(10);
        color: #fff;
        font-size: size-m(12);
        @media (min-width: 768px) {
          bottom: size(15);
          left: size(25);
          font-size: size(16);
        }
      }
    }

    .slide-prev, .slide-next {
      width: size-m(31);
      cursor: pointer;
      position: absolute;
      top: 50%;
      left: size-m(14);
      transform: translate(0, -50%);
      z-index: 1;
      @media (min-width: 768px) {
        width: size(31);
        top: auto;
        bottom: 0;
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
        right: auto;
        left: 8.3vw;
      }
    }

    .swiper-pagination {
      display: none;
      @media (min-width: 768px) {
        display: block;
        width: 6vw;
        bottom: -2.5vw;
        margin-left: 2vw;
      }

      .swiper-pagination-bullet {
        width: size(8);
        height: size(8);
        margin: 0 size(5) !important;
        background: #E5005C;
      }
    }
  }

  .content {
    @media (min-width: 768px) {
      width: size(356);
      padding-bottom: size(52);
    }
  }
  
  .room-btns {
    width: size-m(281);
    margin: size-m(26) auto;
    @media (min-width: 768px) {
      width: size(356);
      margin: 0;
    }

    .room-btn {
      width: size-m(124);
      border: size-m(1) solid #E5005C;
      color: #E5005C;
      font-size: size-m(16);
      line-height: size-m(38);
      text-align: center;
      cursor: pointer;
      transition: all .2s;
      @media (min-width: 768px) {
        width: size(170);
        border: size(1) solid #E5005C;
        font-size: size(28);
        line-height: size(50);
      }

      &:hover, &.active {
        background: #E5005C;
        color: #fff;
      }

      span {
        font-size: size-m(28);
        @media (min-width: 768px) {
          font-size: size(32);
        }
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
import 'swiper/css/pagination';
import { Autoplay, Navigation, Pagination } from "swiper";
const modules = ref([Autoplay, Navigation, Pagination]);
const swiperRef1 = ref(null);
const swiperRef2 = ref(null);
const room = ref(2);

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