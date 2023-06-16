<script>
export default {
   props: {
      mainText: {
         String,
         default: 'footer text',
      }
   }
}
</script>
<template>
   <h3
      class=" w-[160px] text-neo-dark-blue hover:text-neo-cyan text-[18px] leading-[30px] tracking-[.14px] cursor-pointer select-none">
      {{ mainText }}
   </h3>
</template>