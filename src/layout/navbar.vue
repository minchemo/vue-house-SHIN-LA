<template>
    <header id="header">
        <div class="nav-links">
            <div class="nav-item" @click="scrollTo('.s1')">
                <img class="nav-logo" src="@/assets/nav-logo.svg" />
            </div>
            <div class="nav-item" @click="scrollTo('.s2')">
                <div>宏普建設<span class="text-[#A32424]">×</span>三井不動產</div>
            </div>
            <div class="nav-item" @click="scrollTo('.s3')">
                <div>東京質地</div>
            </div>
            <div class="nav-item" @click="scrollTo('.order')">
                <div>預約表單</div>
            </div>
            <div class="nav-item" @click="scrollTo('.s1')">
                <img class="nav-logo2" src="@/assets/nav-logo2.svg" />
            </div>
        </div>
        <div class="nav-btn" @click="menuOpen = !menuOpen">
            <img v-if="menuOpen" src="@/assets/nav-close.svg" />
            <img v-else src="@/assets/nav-menu.svg" />
        </div>
    </header>

    <div id="mob-panel" :class="{open: menuOpen}">
        <div class="nav-close" @click="menuOpen = false">
            <img src="@/assets/nav-close-w.svg" />
        </div>
        <div>
            <div class="nav-item" @click="scrollTo('.s1')">
                <div class="t1">首頁</div>
                <div class="t2">HOME PAGE</div>
            </div>
            <div class="nav-item" @click="scrollTo('.s2')">
                <div class="t1">宏普建設×三井不動產 </div>
                <div class="t2">HONG-PU & MITSUI </div>
            </div>
            <div class="nav-item" @click="scrollTo('.s3')">
                <div class="t1">東京質地</div>
                <div class="t2">LOCATION</div>
            </div>
            <div class="nav-item" @click="scrollTo('.order')">
                <div class="t1">預約表單</div>
                <div class="t2">BOOK NOW</div>
            </div>
        </div>
    </div>

    <div id="desktop-panel" :class="{open: menuOpen}">
        <div class="nav-item">
            <img class="w-full block" src="@/assets/location.svg" />
        </div>
        <div class="nav-item">
            <img class="w-full block" src="@/assets/phone.svg" />
        </div>
        <div class="nav-item">
            <img class="w-full block" src="@/assets/messenger.svg" />
        </div>
    </div>
</template>


<style lang="scss">
@import "@/assets/style/function.scss";

#header {
    position: fixed;
    top: 0;
    right: 0;
    z-index: 99;
    @media (min-width: 768px) {
        width: 100%;
        height: size(160);
        background: #fff;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 0 0 size(59);
    }

    .nav-links {
        display: none;
        @media (min-width: 768px) {
            display: flex;
            align-items: center;
            font-size: size(21);
            font-weight: 600;
            letter-spacing: .23em;
            font-family: "Noto Serif TC";
            color: #000;
        }

        .nav-item {
            &>div {
                border-left: size(1) solid #A32424;
                padding: 0 size(34);
                cursor: pointer;
            }

            &:nth-last-child(2)>div {
                border-right: size(1) solid #A32424;
            }
        }

        .nav-logo {
            width: size(179.73);
            margin-right: size(53.27);
        }

        .nav-logo2 {
            width: size(681.63);
            margin-left: size(68);
        }
    }   

    .nav-btn {
        width: size-m(88);
        height: size-m(88);
        background: #EBECC5;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        @media (min-width: 768px) {
            width: size(160);
            height: size(160);
        }

        img {
            width: size-m(36.64);
            @media (min-width: 768px) {
                width: size(42.48);
            }
        }
    }
}

#mob-panel {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(183deg, #931F1C 42.05%, #7D1E17 178%);
    z-index: 99;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: transform .4s;
    transform: translateX(100%);
    @media (min-width: 768px) {
        display: none;
    }
    
    &.open {
        transform: translateX(0);
    }

    .nav-close {
        width: size-m(88);
        height: size-m(88);
        position: absolute;
        top: 0;
        right: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;

        img {
            display: block;
            width: size-m(30.66);
        }
    }

    .nav-item {
        border-bottom: size-m(1) solid #fff;
        padding-bottom: size-m(20);
        margin-bottom: size-m(20);
        cursor: pointer;

        .t1 {
            color: #fff;
            font-family: "Noto Serif TC";
            font-size: size-m(24);
            font-weight: 600;
            letter-spacing: size-m(3.36);
        }

        .t2 {
            color: #E9C468;
            font-size: size-m(12);
            font-weight: 500;
            letter-spacing: size-m(1.92);
        }
    }
}

#desktop-panel {
    display: none;
    @media (min-width: 768px) {
        display: block;
        position: fixed;
        top: size(160);
        right: 0;
        width: size(160);
        background: linear-gradient(0deg, rgba(235, 236, 197, 0.50) 16%, rgba(235, 245, 207, 0.80) 70%);
        z-index: 99;
        transform: scaleY(0);
        transform-origin: top;
        transition: transform .4s;

        &.open {
            transform: scaleY(1);
        }
    }

    .nav-item {
        cursor: pointer;
    }
}
</style>

<script setup>
import { inject, ref } from 'vue';
import info from "@/info"

const menuOpen = ref(false);
const smoothScroll = inject('smoothScroll');

console.log(info);

const scrollTo = (el) => {
    smoothScroll({
        scrollTo: document.querySelector(el)
    })
    menuOpen.value = false;
}
</script>