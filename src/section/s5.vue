<template>
  <section class="s5 user-n w-full relative">
    <div class="txt absolute">
      <div class="t1 text-[#981F23] md:text-white" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0">
        過去を捨てなくては、<br>
        未来の場所がない
      </div>
      <div class="t2t3" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0">
        <div class="t2 text-[#000000] md:text-white">
          大通膨時代再起，優勢<br>
          資產自住、置產代代相傳
        </div>
        <div class="t3 text-[#000000] md:text-white">原物料推升資產價值，資金穩定停泊最佳去處；優質資產抗通膨、避險保值安心一輩子。</div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
@import "@/assets/style/function.scss";

.s5 {
  width: 100%;
  height: size-m(810);
  background-image: url(@/section/s5/bg-m.webp);
  background-size: cover;
  @media (min-width: 768px) {
    height: size(1022);
    background-image: url(@/section/s5/bg.webp);
  }

  .txt {
    top: size-m(77);
    left: size-m(52);
    width: size-m(296);
    @media (min-width: 768px) {
      display: flex;
      justify-content: space-between;
      top: size(297);
      left: size(384);
      width: size(1323);
    }

    .t1 {
      font-family: "Noto Sans JP";
      font-size: size-m(25);
      font-weight: 700;
      line-height: 157.8%;
      letter-spacing: size-m(3.75);
      margin-bottom: size-m(32);
      @media (min-width: 768px) {
        font-size: size(51);
        font-weight: 700;
        line-height: normal;
        letter-spacing: size(17.34);
        margin-bottom: 0;
        width: size(695);
      }
    }

    .t2t3 {
      @media (min-width: 768px) {
        width: size(586);
      }
    }

    .t2 {
      font-size: size-m(23);
      font-weight: 500;
      line-height: normal;
      margin-bottom: size-m(14);
      @media (min-width: 768px) {
        font-size: size(51);
        margin-bottom: size(46);
      }
    }

    .t3 {
      font-family: "Noto Sans JP";
      font-size: size-m(12);
      font-weight: 500;
      line-height: 210.6%;
      letter-spacing: size-m(0.24);
      @media (min-width: 768px) {
        font-size: size(26);
        line-height: 163.6%;
        letter-spacing: size(0.52);
      }
    }
  }
}
</style>

<script setup>
import { inject } from 'vue';
const smoothScroll = inject('smoothScroll')
const scrollTo = (el) => {
  smoothScroll({
    scrollTo: document.querySelector(el)
  })
}
</script>
