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
               wSize: 'w-[139px]',
            },
            {
               logo: logoImb,
               wSize: 'w-[121px]',
            },
            {
               logo: logoMicrosoft,
               wSize: 'w-[135px]',
            },
            {
               logo: logoHp,
               wSize: 'w-[113px]',
            },
            {
               logo: logoVg,
               wSize: 'w-[105px]',
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
