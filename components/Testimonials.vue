<script>
import imgPhotoEmily from '@/assets/images/image-emily.jpg'
import imgPhotoThomas from '@/assets/images/image-thomas.jpg'
import imgPhotoJennie from '@/assets/images/image-jennie.jpg'
export default {
   data() {
      return {
         imgPhotoEmily,
         imgPhotoThomas,
         imgPhotoJennie,
         data: [
            {
               photo: imgPhotoEmily,
               main: 'We put our trust in Sunnyside and they delivered, making sure our needs were met and deadlines were always hit.',
               name: 'Emily R.',
               occupation: 'Marketing Director',
            },
            {
               photo: imgPhotoThomas,
               main: 'Sunnyside’s enthusiasm coupled with their keen interest in our brand’s success made it a satisfying and enjoyable experience.',
               name: 'Thomas S.',
               occupation: 'Chief Operating Officer',
            },
            {
               photo: imgPhotoJennie,
               main: 'Incredible end result! Our sales increased over 400% when we worked with Sunnyside. Highly recommended!',
               name: 'Jennie F.',
               occupation: 'Business Owner',
            },
         ],
      }
   },
   props: {
      dataIndex: {
         Number,
         default: 0,
      }
   }
}
</script>
<template>
   <div class=" flex flex-col items-center gap-8 DTL:gap-0 DTL:w-[350px] bg-red-200">
      <img class=" w-[72px] DTL:mb-[58px] rounded-full" :src="data[dataIndex].photo" alt="imgPhotoEmily" draggable="false">
      <p class=" DTL:mb-[69px] text-neo-very-dark-grayish-blue text-[18px] leading-[32px] tracking-[-.13px] font-semibold">
         {{ data[dataIndex].main }}
      </p>
      <div class=" flex flex-col gap-[9px]">
         <h4
            class=" text-neo-very-dark-desaturated-blue text-[18px] leading-[18px] tracking-[-.13px] font-fraunces font-black">
            {{ data[dataIndex].name }}
         </h4>
         <h5 class=" text-neo-grayish-blue text-[14px] leading-[25px] tracking-[-.1px] font-semibold">
            {{ data[dataIndex].occupation }}
         </h5>
      </div>
   </div>
</template>