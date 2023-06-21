<script>
export default {
   data() {
      return {
         data: [
            {
               header: 'Transform your brand',
               main: 'We are a full-service creative agency specializing in helping brands grow fast.  Engage your clients through compelling visuals that do most of the marketing for you.',
               color: 'bg-neo-yellow',
            },
            {
               header: 'Stand out to the right audience',
               main: 'Using a collaborative formula of designers, researchers, photographers, videographers, and copywriters, we’ll build and extend your brand in digital places.',
               color: 'bg-neo-soft-red',
            },
         ],
         isHovered: false,
      }
   },
   props: {
      dataIndex: {
         Number,
         default: 0,
      },
      paddingDir: {
         String,
         default: 'left',
      }
   },
   computed: {
      hoverState() {
         return this.isHovered ? 'opacity-[1]' : 'opacity-[.25]';
      },
      paddingState() {
         return this.paddingDir == 'left' ? 'DTL:pl-[165px] DTL:pr-[110px]' : 'DTL:pl-[110px] DTL:pr-[165px]';
      }
   }
}
</script>
<template>
   <div
      :class="` flex flex-col items-center DTL:items-start bg-neo-color-one px-6 MBL:px-10 ${paddingState} py-16 DTL:py-[158px] text-center DTL:text-left`">
      <h2
         class=" mb-6 DTL:mb-8 text-neo-very-dark-desaturated-blue text-[32px] DTL:text-[40px] leading-[47px] tracking-[-.23px] DTL:tracking-[-.29px] font-fraunces font-black">
         {{ data[dataIndex].header }}
      </h2>
      <p class=" mb-8 DTL:mb-10 text-[18px] leading-[30px] tracking-[-.13px] font-semibold">
         {{ data[dataIndex].main }}
      </p>
      <button @mouseenter="isHovered = true" @mouseleave="isHovered = false"
         class=" relative w-[137px] text-neo-very-dark-desaturated-blue text-[15px] leading-[25px] tracking-[1px] font-fraunces font-black uppercase z-10">
         <div :class="` absolute bottom-0 w-full h-[10px] ${data[dataIndex].color} ${hoverState} rounded-[28px] -z-10`">
         </div>
         Learn more
      </button>
   </div>
</template>