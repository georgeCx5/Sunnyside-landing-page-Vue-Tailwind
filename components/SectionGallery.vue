<script>
import imgGbottles from '@/assets/images/mobile/image-gallery-milkbottles.jpg';
import imgGbottlesDTL from '@/assets/images/desktop/image-gallery-milkbottles.jpg';
import imgGOrange from '@/assets/images/mobile/image-gallery-orange.jpg';
import imgGOrangeDTL from '@/assets/images/desktop/image-gallery-orange.jpg';
import imgGCone from '@/assets/images/mobile/image-gallery-cone.jpg';
import imgGConeDTL from '@/assets/images/desktop/image-gallery-cone.jpg';
import imgGsugar from '@/assets/images/mobile/image-gallery-sugar-cubes.jpg';
import imgGsugarDTL from '@/assets/images/desktop/image-gallery-sugarcubes.jpg';
export default {
   data() {
      return {
         imgGbottles,
         imgGOrange,
         imgGCone,
         imgGsugar,
         imgGbottlesDTL,
         imgGOrangeDTL,
         imgGConeDTL,
         imgGsugarDTL,
         width: document.documentElement.clientWidth,
      }
   }
}
</script>
<template>
   <div class=" MBL:max-w-[450px] DTL:max-w-screen-DTL">
      <div class=" grid DTL:hidden grid-cols-2">
         <img :src="imgGbottles" alt="imgGbottles">
         <img :src="imgGOrange" alt="imgGOrange">
         <img :src="imgGCone" alt="imgGCone">
         <img :src="imgGsugar" alt="imgGsugar">
      </div>
      <div class=" hidden DTL:grid DTL:grid-cols-4">
         <img :src="imgGbottlesDTL" alt="imgGbottles">
         <img :src="imgGOrangeDTL" alt="imgGOrange">
         <img :src="imgGConeDTL" alt="imgGCone">
         <img :src="imgGsugarDTL" alt="imgGsugar">
      </div>
   </div>
</template>