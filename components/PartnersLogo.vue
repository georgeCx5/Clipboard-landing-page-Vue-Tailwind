<script>
import logoGoogle from '@/assets/images/logo-google.png';
import logoImb from '@/assets/images/logo-ibm.png';
import logoMicrosoft from '@/assets/images/logo-microsoft.png';
import logoHp from '@/assets/images/logo-hp.png';
import logoVg from '@/assets/images/logo-vector-graphics.png';

export default {
   data() {
      return {
         data: [
            {
               logo: logoGoogle,
               wSize: 'w-[139px] DTL:w-[165px]',
            },
            {
               logo: logoImb,
               wSize: 'w-[121px] DTL:w-[144px]',
            },
            {
               logo: logoMicrosoft,
               wSize: 'w-[135px] DTL:w-[160px]',
            },
            {
               logo: logoHp,
               wSize: 'w-[113px] DTL:w-[134px]',
            },
            {
               logo: logoVg,
               wSize: 'w-[105px] DTL:w-[125px]',
            },
         ]
      }
   },
   props: {
      logoIndex: {
         Number,
         default: 0
      }
   }
}
</script>
<template>
   <img :class="`${data[logoIndex].wSize}`" :src="data[logoIndex].logo" alt="logo image" draggable="false">
</template>
