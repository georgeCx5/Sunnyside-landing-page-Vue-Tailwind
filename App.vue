<script>
import NavBtn from './components/NavBtn.vue';
import SectionText from './components/SectionText.vue';

import Logo from '@/assets/images/logo.svg?component';
import IconHamburger from '@/assets/images/icon-hamburger.svg?component';
import IconArrow from '@/assets/images/icon-arrow-down.svg?component';

import imgEgg from '@/assets/images/mobile/image-transform.jpg';
import imgGlass from '@/assets/images/mobile/image-stand-out.jpg';

export default {
  data() {
    return {
      imgHeaderMB: 'bg-[url(@/assets/images/mobile/image-header.jpg)]',
      imgCherry: 'bg-[url(@/assets/images/mobile/image-graphic-design.jpg)]',
      imgEgg,
      imgGlass,
      isBarOpen: false,
    }
  },
  components: {
    NavBtn,
    SectionText,

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
    <header
      :class="` ${imgHeaderMB} bg-contain relative flex flex-col gap-[88px] w-[375px] h-[538px] px-6 py-8 bg-green-400`">
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

      <!-- Hacer componente de esto -->
      <div
        :class="` flex flex-col justify-end gap-[27px] h-[600px] ${imgCherry} bg-contain px-6 pb-14 text-neo-dark-desaturated-cyan text-center`">
        <h2 class=" text-[28px] leading-[36px] tracking-[-.2px] font-fraunces font-black">
          Graphic design
        </h2>
        <p class=" text-[16px] leading-[27px] tracking-[-.11px] font-semibold">
          Great design makes you memorable. We deliver artwork that underscores your brand message and captures potential
          clients’ attention.
        </p>
      </div>
    </main>
  </body>
</template>
<style>
.g {
  color: hsl(167, 40%, 24%);
}
</style>