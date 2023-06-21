<script>
export default {
   data() {
      return {

      }
   },
   props: {
      btnText: {
         String,
         default: 'empty text',
      }
   }
}
</script>
<template>
   <button
      class=" text-neo-white hover:text-neo-very-dark-desaturated-blue text-[18px] leading-[25px] tracking-[-.13px] font-semibold">
      {{ btnText }}
   </button>
</template>