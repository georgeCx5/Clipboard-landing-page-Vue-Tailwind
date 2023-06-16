<script>
export default {
   data() {
      return {
         data: [
            {
               header: 'Quick Search',
               main: 'Easily search your snippets by content, category, web address, application, and more.',
            },
            {
               header: 'iCloud Sync',
               main: 'Instantly saves and syncs snippets across all your devices.',
            },
            {
               header: 'Complete History',
               main: 'Retrieve any snippets from the first moment you started using the app.',
            },
         ]
      }
   },
   props: {
      dataIndex: Number,
   }
}
</script>
<template>
   <div class=" flex flex-col gap-[10px]">
      <h3 class=" text-neo-dark-blue text-[24px] leading-[30px] tracking-[-.39px] font-semibold">
         {{ data[dataIndex].header }}
      </h3>
      <p class=" text-[16px] leading-[26px] tracking-[.12px]">
         {{ data[dataIndex].main }}
      </p>
   </div>
</template>