<template>
    <div class="houseinfo md:flex md:items-center md:justify-between bg-[#E5005C]">
        <img class="logo" src="@/section/form/logo.svg" />
        <div class="info-box" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0">
            <div class="title">建案資訊</div>
            <div class="info-items">
                <div class="item flex justify-between items-center w-full whitespace-nowrap"
                    v-for="item in info.houseInfos">
                    <p>{{ item[0] }}</p>
                    <p>{{ item[1] }}</p>
                </div>
            </div>
        </div>
    </div>
    <!--div class="footer flex items-center justify-center w-full h-[40px] bg-[#302626]">
        <a href="https://www.lixin.com.tw/" target="_blank"><img class="hover:opacity-50"
                src="@/section/form/footerlogo.gif" alt="Lixin" srcset=""></a>
        <a href="https://www.h65.tw/admin/test/login" target="_blank"><p class="text-white text-xs">網頁製作</p></a>
    </div-->
</template>

<style lang="scss">
@import "@/assets/style/function.scss";

.houseinfo {
    color: #fff;
    background: #C30D23;
    padding: size(30) size(228) size(60);
    @media screen and (max-width:768px) {
        padding: size-m(69) size-m(50);
    }

    .logo {
        width: size(494.42);
        @media screen and (max-width:768px) {
            width: size-m(223);
            margin: 0 auto size-m(62) auto;
        }
    }
}

.info-box {
    width: size(680);

    .title {
        width: 100%;
        font-size: size(29);
        font-weight: 500;
        line-height: normal;
        letter-spacing: size(1.45);
        margin-bottom: size(12);
        text-align: left;
    }

    .info-items {
        row-gap: size(20);
        column-gap: size(20);

        .item {
            line-height: normal;
            font-size: size(18);
            align-items: flex-start;
            line-height: 1.5;
            text-align: left;
            letter-spacing: size(0.9);
            border-bottom: 1px solid #fff;
            padding-bottom: size(9);
            margin-bottom: size(9);

            &:first-child {
                border-top: 1px solid #fff;
                padding-top: size(9);
            }
        }
    }
}

@media screen and (max-width:768px) {
    .footer {
        margin-bottom: size-m(63);
        display: none;
    }

    .info-box {
        width: size-m(275);
        padding: 0;

        .title {
            font-size: size-m(20);
            margin-bottom: size-m(11);
        }

        .info-items {
            .item {
                font-size: size-m(12);
                letter-spacing: size-m(0);
                padding-bottom: size-m(8);
                margin-bottom: size-m(8);

                &:first-child {
                    border-top: 1px solid #fff;
                    padding-top: size-m(8);
                }
            }
        }
    }

}
</style>

<script setup>
import info from "@/info"


</script>