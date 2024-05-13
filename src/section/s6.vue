<template>
  <section class="s6 user-n w-full relative text-white">
    <img class="logo absolute md:hidden" src="@/section/s6/logo-m.svg" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0" />
    <img class="logo absolute hidden md:block" src="@/section/s6/logo.svg" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0" />
    <div class="txt absolute" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0">
      商道人情萬事起 家邸傳承百事興<br>
      北投站350米｜31-39坪 邊間3房
    </div>
    <div class="t2024 absolute hidden md:block" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0">2024 初夏相見</div>
    <img class="phone absolute" src="@/section/s6/phone.svg" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0" />
    <div class="company absolute flex md:block items-end" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0">
      <img src="@/section/s6/company1.svg" />
      <img src="@/section/s6/company2.svg" />
    </div>
    <img class="jp absolute hidden md:block" src="@/section/s1/jp.svg" />
  </section>
</template>

<style lang="scss">
@import "@/assets/style/function.scss";

.s6 {
  width: 100%;
  height: size-m(779);
  background: #C30D23;
  background-image: url(@/section/s6/bg.png);
  background-position: center;
  background-size: auto 100%;
  @media (min-width: 768px) {
    height: size(1120);
  }

  .logo {
    top: size-m(89.69);
    left: size-m(50);
    width: size-m(276);
    @media (min-width: 768px) {
      top: size(165.48);
      left: size(595);
      width: size(727);
    }
  }

  .txt {
    text-align: center;
    top: size-m(523);
    left: size-m(50);
    font-size: size-m(19);
    font-weight: 500;
    line-height: normal;
    letter-spacing: size-m(0.38);
    @media (min-width: 768px) {
      top: size(692);
      left: size(595);
      font-size: size(50);
      letter-spacing: size(1.5);
    }
  }

  .t2024 {
    @media (min-width: 768px) {
      top: size(896);
      left: size(597);
      font-size: size(33);
      letter-spacing: size(0.99);
    }
  }

  .phone {
    top: size-m(613);
    left: size-m(71);
    width: size-m(232);
    @media (min-width: 768px) {
      top: size(891);
      left: size(863);
      width: size(300);
    }
  }

  .company {
    top: size-m(676);
    left: size-m(95);
    @media (min-width: 768px) {
      top: size(887.35);
      left: size(1220);
    }

    img {
      &:nth-child(1) {
        width: size-m(90.46);
        margin-right: size-m(18.33);
        @media (min-width: 768px) {
          width: size(98.93);
          margin-right: 0;
          margin-bottom: size(15.33);
        }
      }

      &:nth-child(2) {
        width: size-m(76.15);
        @media (min-width: 768px) {
          width: size(98.93);
        }
      }
    }
  }

  .jp {
    @media (min-width: 768px) {
      top: size(135);
      left: size(1804);
      width: size(19.38);
    }
  }
}
</style>

<script setup>
</script>
