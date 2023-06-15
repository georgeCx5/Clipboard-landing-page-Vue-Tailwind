<script>
import BtnHeader from './components/BtnHeader.vue';
import FeaturesOne from './components/FeaturesOne.vue';

import Logo from '@/assets/images/logo.svg?component';

import imgComputer from '@/assets/images/image-computer.png';

export default {
  data() {
    return {
      imgComputer,
    }
  },
  components: {
    BtnHeader,
    FeaturesOne,

    Logo,
  }
}
</script>
<template>
  <body class=" flex flex-col items-center text-neo-grayish-blue font-jamjuree">
    <main class=" flex flex-col items-center w-[311px]">
      <Logo />
      <div class=" text-center">
        <h1 class=" text-neo-dark-blue text-[32px] leading-[40px] tracking-[-.52px] font-semibold">
          A history of everything you copy
        </h1>
        <p class=" text-[16px] leading-[26px] tracking-[.12px]">
          Clipboard allows you to track and organize everything you
          copy. Instantly access your clipboard on all your devices.
        </p>
      </div>
      <div class=" flex flex-col gap-6 w-full text-white text-[18px] leading-[30px] tracking-[.5px] font-semibold">
        <BtnHeader btnText="iOS" bgColor="bg-neo-cyan" />
        <BtnHeader btnText="Mac" bgColor="bg-neo-blue" />
      </div>
      <div>
        <h2 class=" text-neo-dark-blue text-[28px] leading-[35px] tracking-[-.52px] font-semibold">
          Keep track of your snippets
        </h2>
        <p class=" text-[16px] leading-[26px] tracking-[.12px]">
          Clipboard instantly stores any item you copy in the cloud,
          meaning you can access your snippets immediately on all your
          devices. Our Mac and iOS apps will help you organize everything.
        </p>
      </div>
      <div>
        <img :src="imgComputer" alt="imgComputer">
        <div class=" flex flex-col gap-12">
          <FeaturesOne :dataIndex="0" />
          <FeaturesOne :dataIndex="1" />
          <FeaturesOne :dataIndex="2" />
        </div>
      </div>
    </main>
  </body>
</template>