<script>
import IconBlacklist from '@/assets/images/icon-blacklist.svg?component';
import IconText from '@/assets/images/icon-text.svg?component';
import IconPreview from '@/assets/images/icon-preview.svg?component';

export default {
   data() {
      return {
         data: [
            {
               header: 'Create blacklists',
               main: 'Ensure sensitive information never makes its way to your clipboard by excluding certain sources.',
               icon: 'IconBlacklist',
            },
            {
               header: 'Plain text snippets',
               main: 'Remove unwanted formatting from copied text for a consistent look.',
               icon: 'IconText',
            },
            {
               header: 'Sneak preview',
               main: 'Quick preview of all snippets on your Clipboard for easy access.',
               icon: 'IconPreview',
            },
         ]
      }
   },
   components: {
      IconBlacklist,
      IconText,
      IconPreview,
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
   <div class=" flex flex-col items-center gap-[40px]">
      <component :is="data[dataIndex].icon" />
      <div class=" flex flex-col gap-[18px]">
         <h3 class=" text-neo-dark-blue text-[24px] leading-[30px] tracking-[-.39px] font-semibold">
            {{ data[dataIndex].header }}
         </h3>
         <p class=" text-[16px] leading-[26px] tracking-[.12px]">
            {{ data[dataIndex].main }}
         </p>
      </div>
   </div>
</template>