<script>
import NavBtn from './components/NavBtn.vue';
import SectionText from './components/SectionText.vue';
import SectionTextAndImage from './components/SectionTextAndImage.vue';
import Testimonials from './components/Testimonials.vue';
import SectionGallery from './components/SectionGallery.vue';
import FooterLogo from './components/FooterLogo.vue';
import FooterBtn from './components/FooterBtn.vue';
import FooterNetwork from './components/FooterNetwork.vue';

import Logo from '@/assets/images/logo.svg?component';
import IconHamburger from '@/assets/images/icon-hamburger.svg?component';
import IconArrow from '@/assets/images/icon-arrow-down.svg?component';

import imgEgg from '@/assets/images/mobile/image-transform.jpg';
import imgGlass from '@/assets/images/mobile/image-stand-out.jpg';

export default {
  data() {
    return {
      imgHeaderMB: 'bg-[url(@/assets/images/mobile/image-header.jpg)]',
      imgHeaderDTL: 'DTL:bg-[url(@/assets/images/desktop/image-header.jpg)]',
      imgEgg,
      imgGlass,
      isBarOpen: false,
    }
  },
  components: {
    NavBtn,
    SectionText,
    SectionTextAndImage,
    Testimonials,
    SectionGallery,
    FooterLogo,
    FooterBtn,
    FooterNetwork,

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
      :class="` ${imgHeaderMB} ${imgHeaderDTL} bg-cover relative flex flex-col gap-[88px] DTL:w-full min-w-[375px] MBL:max-w-[450px] DTL:max-w-screen-DTL h-[538px] DTL:h-[800px] px-6 py-8`">
      <nav class=" relative flex justify-between">
        <Logo />
        <IconHamburger @click="isBarOpen = !isBarOpen" :class="` DTL:hidden ${barState} cursor-pointer`" />
        <!-- Mobile Bar -->
        <div v-show="isBarOpen" class=" absolute right-0 top-[50px] DTL:hidden pointer-events-none">
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
        <!--  -->
      </nav>
      <div class=" flex flex-col items-center gap-[52px] text-center">
        <h1 class=" text-neo-white text-[40px] leading-[47px] tracking-[6.25px] font-black font-fraunces uppercase">
          We are creatives
        </h1>
        <IconArrow />
      </div>
    </header>
    <main class=" grid grid-flow-row grid-cols-1 DTL:grid-cols-2 min-w-[375px] MBL:max-w-[450px] DTL:max-w-screen-DTL">
      <img class=" order-1 DTL:order-2" :src="imgEgg" alt="imgEgg">
      <SectionText class=" order-2 DTL:order-1" :data-index="0" />
      <img class=" order-3" :src="imgGlass" alt="imgGlass">
      <SectionText class=" order-4" :data-index="1" padding-dir="right" />
      <SectionTextAndImage class=" order-5" :data-index="0" />
      <SectionTextAndImage class=" order-6" :data-index="1" />
    </main>
    <section
      class=" flex flex-col gap-16 DTL:gap-[81px] MBL:max-w-[450px] DTL:max-w-screen-DTL px-6 MBL:px-10 py-16 DTL:py-40 bg-neo-color-one text-center">
      <h3 class=" text-[16px] DTL:text-[20px] leading-[18px] DTL:leading-[24px] tracking-[4px] DTL:tracking-[5px] font-fraunces font-black uppercase">Client testimonials</h3>
      <div class=" flex flex-col DTL:flex-row gap-16 DTL:gap-[30px]">
        <Testimonials :data-index="0" />
        <Testimonials :data-index="1" />
        <Testimonials :data-index="2" />
      </div>
    </section>
    <SectionGallery />
    <footer class=" flex flex-col items-center w-full min-w-[375px] MBL:max-w-[450px] pt-16 pb-20 bg-neo-color-two">
      <FooterLogo class=" scale-[1.33] m-[4px] mb-11" />
      <div class=" flex gap-[57px] mb-[88px]">
        <FooterBtn btn-text="About" />
        <FooterBtn btn-text="Services" />
        <FooterBtn btn-text="Projects" />
      </div>
      <div class=" flex gap-7 items-center">
        <FooterNetwork data-name="facebook" />
        <FooterNetwork data-name="instagram" />
        <FooterNetwork data-name="twitter" />
        <FooterNetwork data-name="pinterest" />
      </div>
    </footer>
  </body>
</template>
<style>
.g {
  color: #458c7e
}</style>