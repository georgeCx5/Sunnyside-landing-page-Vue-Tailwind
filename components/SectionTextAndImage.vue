<script>
export default {
   data() {
      return {
         data: [
            {
               header: 'Graphic design',
               main: 'Great design makes you memorable. We deliver artwork that underscores your brand message and captures potential clients’ attention.',
               bgImage: 'bg-[url(@/assets/images/mobile/image-graphic-design.jpg)]',
               textColor: 'text-neo-dark-desaturated-cyan',
            },
            {
               header: 'Photography',
               main: 'Increase your credibility by getting the most stunning, high-quality photos that improve your business image.',
               bgImage: 'bg-[url(@/assets/images/mobile/image-photography.jpg)]',
               textColor: 'text-neo-dark-blue',
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
   <div
      :class="` flex flex-col justify-end gap-[27px] h-[600px] ${data[dataIndex].bgImage} bg-cover px-6 MBL:px-10 pb-14 text-center ${data[dataIndex].textColor}`">
      <h2 class=" text-[28px] leading-[36px] tracking-[-.2px] font-fraunces font-black">
         {{ data[dataIndex].header }}
      </h2>
      <p class=" text-[16px] leading-[27px] tracking-[-.11px] font-semibold">
         {{ data[dataIndex].main }}
      </p>
   </div>
</template>