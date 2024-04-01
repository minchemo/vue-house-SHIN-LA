<template>
  <section class="s15 w-full relative text-[#173868]">
    <img class="bg absolute hidden md:block" src="@/section/s15/bg.webp" />
    <img class="bg absolute md:hidden" src="@/section/s15/bgm.webp" />
    <div class="rect w-full absolute"></div>
    <!--div class="info absolute">情境示意圖</div-->
    <div class="txt text-center">
      <div data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0">
        <div class="title">國際選材 忠於品質</div>
        <div class="subtitle">HIGHEST QUALITY</div>
        <div class="content hidden md:block">
          世界的新資源、高品質<br>
          清景麟通通把它獻給您
        </div>
        <div class="content md:hidden">
          世界的新資源、高品質，清景麟通通把它獻給您
        </div>
      </div>
    </div>
    <div class="logos relative bg-[#173868] hidden md:block" data-aos="logo-fade-up" data-aos-duration="1000" data-aos-delay="0">
       <img class="w-full block" src="@/section/s15/logos.svg" /> 
    </div>

    <div class="logos relative md:hidden" data-aos="logo-fade-up" data-aos-duration="1000" data-aos-delay="0">
       <img class="w-full block" src="@/section/s15/logosm1.svg" /> 
    </div>
  </section>
</template>

<style lang="scss">
@import "@/assets/style/function.scss";

@keyframes logos {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.logos {
  g {
    opacity: 0;
    transform: translateY(100px);
  }
  &.aos-animate g {
    animation-name: logos;
    animation-duration: 1s;
    animation-delay: 0s;
    animation-iteration-count: 1;
    animation-direction: normal;
    animation-timing-function: ease;
    animation-fill-mode: forwards;

    @for $i from 1 through 9 {
      &:nth-child(#{$i}) {
        animation-delay: ($i - 1) * 0.2s;
      }
    }
  }
}


.s15 {
  overflow: hidden;
  font-size: size-m(13);
  font-weight: 500;
  height: size-m(667);
  line-height: size-m(20);
  @media (min-width: 768px) {
    font-size: size(26);
    line-height: normal;
    height: size(1080);
    letter-spacing: size(8.58);
  }

  .bg {
    max-width: none;
    width: size-m(375);
    top: auto;
    bottom: 0;
    left: size-m(0);
    @media (min-width: 768px) {
      width: 100%;
      top: auto;
      bottom: 0;
      left: 0;
    }
  }

  .rect {
    height: size-m(268);
    top: size-m(74);
    left: 0;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.00) 0%, #FFF 54.72%);
    @media (min-width: 768px) {
      display: none;
    }
  }

  .txt {
    padding: size-m(60) size-m(25) size-m(0) size-m(25);
    @media (min-width: 768px) {
      position: absolute;
      top: size(128);
      left: size(160);
      width: size(580);
      padding: 0;
    }

    .title {
      font-family: "Noto Serif TC";
      font-size: size-m(30);
      font-weight: 700;
      letter-spacing: size-m(6.9);
      text-indent: size-m(6.9);
      margin-bottom: size-m(5);
      line-height: normal;
      @media (min-width: 768px) {
        font-size: size(48);
        letter-spacing: size(15.84);
        text-indent: size(15.84);
        margin-bottom: size(9);
        padding-bottom: 0;
      }
    }

    .subtitle {
      font-family: "Noto Serif TC";
      font-size: size-m(15);
      font-weight: 700;
      letter-spacing: size-m(5);
      text-indent: size-m(5);
      margin-bottom: size-m(17);
      line-height: normal;
      @media (min-width: 768px) {
        font-size: size(24);
        letter-spacing: size(7.92);
        text-indent: size(7.92);
        margin-bottom: size(52);
      }
    }
  }
  
  .info {
    top: size-m(4);
    left: size-m(4);
    color: #767676;
    font-size: size-m(12);
    line-height: normal;
    @media (min-width: 768px) {
      top: auto;
      bottom: size(10);
      left: auto;
      right: size(10);
      font-size: size(12);
      letter-spacing: 0;
    }
  }

  .logos {
    padding: size-m(50) size-m(30);
    @media (min-width: 768px) {
      position: absolute;
      top: size(456);
      left: size(946);
      width: size(866.45);
      border-radius: size(30);
      padding: size(45) size(130);
    }
  }
}
</style>

<script setup>
</script>