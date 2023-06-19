<script>
import NavBtn from './components/NavBtn.vue';
import SectionText from './components/SectionText.vue';
import SectionTextAndImage from './components/SectionTextAndImage.vue';
import Testimonials from './components/Testimonials.vue';

import Logo from '@/assets/images/logo.svg?component';
import IconHamburger from '@/assets/images/icon-hamburger.svg?component';
import IconArrow from '@/assets/images/icon-arrow-down.svg?component';

import imgEgg from '@/assets/images/mobile/image-transform.jpg';
import imgGlass from '@/assets/images/mobile/image-stand-out.jpg';
// import imgPhotoEmily from '@/assets/images/image-emily.jpg'

export default {
  data() {
    return {
      imgHeaderMB: 'bg-[url(@/assets/images/mobile/image-header.jpg)]',
      imgEgg,
      imgGlass,
      isBarOpen: false,
      // imgPhotoEmily,
    }
  },
  components: {
    NavBtn,
    SectionText,
    SectionTextAndImage,
    Testimonials,

    Logo,
    IconHamburger,
    IconArrow,
  },
  computed: {
    barState() {
      return this.isBarOpen ? 'opacity-[.5]' : 'opacity-[1]';
    }
  }
}
</script>
<template>
  <body class=" flex flex-col items-center text-neo-dark-grayish-blue font-barlow">
    <header :class="` ${imgHeaderMB} bg-contain relative flex flex-col gap-[88px] w-[375px] h-[538px] px-6 py-8`">
      <nav class=" relative flex justify-between">
        <Logo />
        <IconHamburger @click="isBarOpen = !isBarOpen" :class="`  ${barState} cursor-pointer`" />
        <div v-show="isBarOpen" class=" absolute right-0 top-[50px] pointer-events-none">
          <div
            class=" absolute right-0 top-0 w-0 h-0 border-b-[24px] border-l-[24px] border-transparent border-b-neo-white">
          </div>
          <div
            class=" absolute right-0 top-6 flex flex-col justify-center items-center gap-8 w-[329px] h-[305px] bg-neo-white select-none pointer-events-auto">
            <NavBtn btn-text="About" />
            <NavBtn btn-text="Services" />
            <NavBtn btn-text="Projects" />
            <button
              class=" w-[140px] h-[56px] bg-neo-yellow hover:bg-neo-very-dark-desaturated-blue text-neo-very-dark-desaturated-blue hover:text-neo-white text-[15px] leading-[25px] tracking-[-.11px] font-fraunces font-bold uppercase rounded-[28px]">
              Contact
            </button>
          </div>
        </div>
      </nav>
      <div class=" flex flex-col items-center gap-[52px] text-center">
        <h1 class=" text-neo-white text-[40px] leading-[47px] tracking-[6.25px] font-black font-fraunces uppercase">
          We are creatives
        </h1>
        <IconArrow />
      </div>
    </header>
    <main class=" w-[375px]">
      <img :src="imgEgg" alt="imgEgg">
      <SectionText :data-index="0" />
      <img :src="imgGlass" alt="imgGlass">
      <SectionText :data-index="1" />
      <SectionTextAndImage :data-index="0" />
      <SectionTextAndImage :data-index="1" />
      <div class=" flex flex-col gap-16 px-6 py-16 bg-neo-color-one text-center">
        <h3 class=" text-[16px] leading-[18px] tracking-[4px] font-fraunces font-black uppercase">Client testimonials</h3>
        <Testimonials :data-index="0" />
        <Testimonials :data-index="1" />
        <Testimonials :data-index="2" />
      </div>
    </main>
  </body>
</template>
<style>
.g {
  color: hsl(213, 9%, 39%);
}
</style>