<script>
import imgGbottles from '@/assets/images/mobile/image-gallery-milkbottles.jpg';
import imgGOrange from '@/assets/images/mobile/image-gallery-orange.jpg';
import imgGCone from '@/assets/images/mobile/image-gallery-cone.jpg';
import imgGsugar from '@/assets/images/mobile/image-gallery-sugar-cubes.jpg';
export default {
   data() {
      return {
         imgGbottles,
         imgGOrange,
         imgGCone,
         imgGsugar,
      }
   }
}
</script>
<template>
   <div class=" grid grid-cols-2 w-full">
      <img :src="imgGbottles" alt="imgGbottles">
      <img :src="imgGOrange" alt="imgGOrange">
      <img :src="imgGCone" alt="imgGCone">
      <img :src="imgGsugar" alt="imgGsugar">
   </div>
</template>