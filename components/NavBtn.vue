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
   <button class=" hover:text-neo-very-dark-desaturated-blue text-[20px] leading-[25px] tracking-[-.14px] font-semibold">
      {{ btnText }}
   </button>
</template>
<style>
.test{
   color: hsl(232, 10%, 55%);
}
</style>