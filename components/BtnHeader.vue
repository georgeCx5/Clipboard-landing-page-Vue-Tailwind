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
   <div class=" relative">
      <button :class="` w-full h-14 ${bgColor} hover:brightness-[1.25] peer rounded-[28px]`">
         Download for {{ btnText }}
      </button>
      <div
         :class="` absolute top-1 w-full h-full ${bgColor} brightness-[.85] peer-hover:brightness-[1] rounded-[28px] -z-10`">
      </div>
   </div>
</template>