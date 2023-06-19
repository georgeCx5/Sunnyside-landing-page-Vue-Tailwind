<script>
export default {
   props: {
      btnText: {
         String,
         default: 'empty btn',
      }
   }
}
</script>
<template>
   <button class="text-neo-dark-moderate-cyan hover:text-neo-white text-[18px] leading-[25px] tracking-[-.13px] font-semibold">
      {{ btnText }}
   </button>
</template>