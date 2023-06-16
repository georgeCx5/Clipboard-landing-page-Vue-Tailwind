<script>
export default {
   props: {
      btnText: {
         String,
         default: 'Symbian',
      },
      bgColor: {
         String,
         default: 'bg-red-200',
      },
   }
}
</script>
<template>
   <div class=" relative text-white text-[18px] leading-[30px] tracking-[.5px] font-semibold">
      <button :class="` w-full h-[52px] ${bgColor} hover:brightness-[1.25] peer rounded-[28px]`">
         Download for {{ btnText }}
      </button>
      <div
         :class="` absolute top-[6px] w-full h-full ${bgColor} brightness-[.85] peer-hover:brightness-[1] rounded-[28px] -z-10`">
      </div>
   </div>
</template>