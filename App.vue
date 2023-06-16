<script>
import BtnHeader from './components/BtnHeader.vue';
import FeaturesOne from './components/FeaturesOne.vue';
import FeaturesTwo from './components/FeaturesTwo.vue';
import PartnersLogo from './components/PartnersLogo.vue';
import FooterText from './components/FooterText.vue';
import NetworkIcon from './components/NetworkIcon.vue';

import Logo from '@/assets/images/logo.svg?component';

import bgMobile from '@/assets/images/bg-header-mobile.png';
import bgDesktop from '@/assets/images/bg-header-desktop.png';
import imgComputer from '@/assets/images/image-computer.png';
import imgDevices from '@/assets/images/image-devices.png';

export default {
  data() {
    return {
      bgMobile,
      bgDesktop,
      imgComputer,
      imgDevices,
    }
  },
  components: {
    BtnHeader,
    FeaturesOne,
    FeaturesTwo,
    PartnersLogo,
    FooterText,
    NetworkIcon,

    Logo,
  }
}
</script>
<template>
  <body class=" flex flex-col items-center text-neo-grayish-blue font-jamjuree">
    <main class=" relative flex flex-col items-center min-w-[375px] max-w-[525px] TB:min-w-[768px] TB:max-w-[1024px] px-8 TB:px-16 py-32">
      <div class=" absolute top-0">
        <img class=" DT:hidden w-screen" :src="bgMobile" alt="bgMobile" draggable="false">
        <img class=" hidden DT:block" :src="bgDesktop" alt="bgDesktop" draggable="false">
      </div>
      <div class=" flex flex-col items-center gap-[64px] mb-[160px] ">
        <Logo />
        <div class=" flex flex-col gap-[48px]">
          <div class=" flex flex-col gap-[16px] TB:px-12 text-center">
            <h1 class=" text-neo-dark-blue text-[32px] leading-[40px] tracking-[-.52px] font-semibold">
              A history of everything you copy
            </h1>
            <p class=" text-[16px] leading-[26px] tracking-[.12px]">
              Clipboard allows you to track and organize everything you
              copy. Instantly access your clipboard on all your devices.
            </p>
          </div>
          <div class=" flex flex-col TB:flex-row TB:justify-center gap-6 TB:gap-4 w-full">
            <BtnHeader btnText="iOS" bgColor="bg-neo-cyan" />
            <BtnHeader btnText="Mac" bgColor="bg-neo-blue" />
          </div>
        </div>
      </div>
      <div class=" flex flex-col gap-[65px] mb-[186px]">
        <div class=" flex flex-col gap-4 TB:px-12 text-center">
          <h2 class=" text-neo-dark-blue text-[28px] leading-[35px] tracking-[-.52px] font-semibold">
            Keep track of your snippets
          </h2>
          <p class=" text-[16px] leading-[26px] tracking-[.12px]">
            Clipboard instantly stores any item you copy in the cloud,
            meaning you can access your snippets immediately on all your
            devices. Our Mac and iOS apps will help you organize everything.
          </p>
        </div>
        <div class=" TB:relative -left-12 flex flex-col TB:flex-row gap-14">
          <img class=" TB:w-[50%] object-contain" :src="imgComputer" alt="imgComputer" draggable="false">
          <div class=" flex flex-col gap-12 text-center TB:text-left">
            <FeaturesOne :dataIndex="0" />
            <FeaturesOne :dataIndex="1" />
            <FeaturesOne :dataIndex="2" />
          </div>
        </div>
      </div>
      <div class=" flex flex-col TB:items-center gap-16 mb-[130px]">
        <div class=" flex flex-col gap-4 TB:px-12 text-center">
          <h2 class=" text-neo-dark-blue text-[28px] leading-[35px] tracking-[-.46px] font-semibold">
            Access Clipboard anywhere
          </h2>
          <p class=" text-[16px] leading-[26px] tracking-[.12px]">
            Whether you’re on the go, or at your computer, you can access all your Clipboard
            snippets in a few simple clicks.
          </p>
        </div>
        <img class=" TB:w-[80%]" :src="imgDevices" alt="imgDevices" draggable="false">
      </div>
      <div class=" flex flex-col gap-[90px] mb-[130px]">
        <div class=" flex flex-col gap-[11px] text-center">
          <h2 class=" text-neo-dark-blue text-[28px] leading-[35px] tracking-[-.46px] font-semibold">
            Supercharge your workflow
          </h2>
          <p class=" text-[16px] leading-[26px] tracking-[.12px]">
            We’ve got the tools to boost your productivity.
          </p>
        </div>
        <div class=" flex flex-col gap-14 TB:px-32 text-center">
          <FeaturesTwo dataIndex="0" />
          <FeaturesTwo dataIndex="1" />
          <FeaturesTwo dataIndex="2" />
        </div>
      </div>
      <div class=" flex flex-col items-center gap-14 mb-[170px]">
        <PartnersLogo :logoIndex="0" />
        <PartnersLogo :logoIndex="1" />
        <PartnersLogo :logoIndex="2" />
        <PartnersLogo :logoIndex="3" />
        <PartnersLogo :logoIndex="4" />
      </div>
      <div class=" flex flex-col gap-[46px]">
        <div class=" flex flex-col gap-4 TB:px-12 text-center">
          <h2 class=" text-neo-dark-blue text-[28px] leading-[35px] tracking-[-.46px] font-semibold">
            Clipboard for iOS and Mac OS
          </h2>
          <p class=" text-[16px] leading-[26px] tracking-[.12px]">
            Available for free on the App Store. Download for Mac or iOS, sync with iCloud
            and you’re ready to start adding to your clipboard.
          </p>
        </div>
        <div class=" flex flex-col TB:flex-row TB:justify-center gap-6 TB:gap-4 w-full">
          <BtnHeader btnText="iOS" bgColor="bg-neo-cyan" />
          <BtnHeader btnText="Mac" bgColor="bg-neo-blue" />
        </div>
      </div>
    </main>
    <footer class=" flex flex-col items-center gap-10 TB:gap-16 w-full py-[52px] bg-neo-grayish-blue bg-opacity-10">
      <logo class=" scale-[.44] -m-[35px]" />
      <div class=" flex flex-col TB:flex-row items-center TB:items-start gap-12 TB:gap-24">
        <div class=" flex flex-col gap-5 text-center TB:text-left">
          <FooterText mainText="FAQs" />
          <FooterText mainText="Contact Us" />
          <FooterText mainText="Privacy Policy" />
          <FooterText mainText="Press Kit" />
          <FooterText mainText="Install Guide" />
        </div>
        <div class=" flex gap-10">
          <NetworkIcon iconName="facebook" />
          <NetworkIcon iconName="twitter" />
          <NetworkIcon iconName="instagram" />
        </div>
      </div>
    </footer>
  </body>
</template>