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
  <body class=" flex flex-col items-center text-neo-grayish-blue font-jamjuree overflow-hidden">
    <main
      class=" relative flex flex-col items-center min-w-[375px] max-w-[525px] TB:min-w-[768px] TB:max-w-[1024px] DTL:min-w-[1440px] DTL:max-w-[1920px] px-8 TB:px-16 py-32 DTL:pb-36">
      <div class=" absolute top-0">
        <img class=" DTL:hidden w-screen" :src="bgMobile" alt="bgMobile" draggable="false">
        <img class=" hidden DTL:block w-screen" :src="bgDesktop" alt="bgDesktop" draggable="false">
      </div>
      <div class=" flex flex-col items-center gap-[64px] DTL:gap-[56px] mb-[160px] DTL:mb-[150px] z-30">
        <Logo />
        <div class=" flex flex-col gap-[48px]">
          <div class=" flex flex-col gap-[16px] TB:px-12 DTL:px-80 text-center">
            <h1
              class=" text-neo-dark-blue text-[32px] DTL:text-[46px] leading-[40px] DTL:leading-[58px] tracking-[-.52px] font-semibold">
              A history of everything you copy
            </h1>
            <p
              class=" text-[16px] DTL:text-[20px] leading-[26px] DTL:leading-[30px] tracking-[.12px] DTL:tracking-[.15px]">
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
      <div class=" flex flex-col gap-[65px] DTL:gap-[80px] mb-[186px] DTL:mb-[150px]">
        <div class=" flex flex-col gap-4 DTL:gap-5 TB:px-12 DTL:px-80 text-center">
          <h2
            class=" text-neo-dark-blue text-[28px] DTL:text-[36px] leading-[35px] DTL:leading-[45px] tracking-[-.52px] DTL:tracking-[-.59px] font-semibold">
            Keep track of your snippets
          </h2>
          <p class=" text-[16px] DTL:text-[18px] leading-[26px] DTL:leading-[30px] tracking-[.12px] DTL:tracking-[.14px]">
            Clipboard instantly stores any item you copy in the cloud,
            meaning you can access your snippets immediately on all your
            devices. Our Mac and iOS apps will help you organize everything.
          </p>
        </div>
        <div
          class=" TB:relative -left-12 DTL:-left-24 flex flex-col TB:flex-row DTL:items-center gap-14 DTL:gap-28 DTL:pr-36">
          <img class=" TB:w-[50%] DTL:w-[752px] object-contain" :src="imgComputer" alt="imgComputer" draggable="false">
          <div class=" flex flex-col gap-12 DTL:gap-14 DTL:-mt-12 text-center TB:text-left">
            <FeaturesOne :dataIndex="0" />
            <FeaturesOne :dataIndex="1" />
            <FeaturesOne :dataIndex="2" />
          </div>
        </div>
      </div>
      <div class=" flex flex-col TB:items-center gap-16 DTL:gap-28 mb-[130px] DTL:mb-16">
        <div class=" flex flex-col gap-4 DTL:gap-5 TB:px-12 DTL:px-80 text-center">
          <h2
            class=" text-neo-dark-blue text-[28px] DTL:text-[36px] leading-[35px] DTL:leading-[45px] tracking-[-.46px] DTL:tracking-[-.59px] font-semibold">
            Access Clipboard anywhere
          </h2>
          <p class=" text-[16px] DTL:text-[18px] leading-[26px] DTL:leading-[30px] tracking-[.12px] DTL:tracking-[.14px]">
            Whether you’re on the go, or at your computer, you can access all your Clipboard
            snippets in a few simple clicks.
          </p>
        </div>
        <img class=" TB:w-[80%] DTL:w-[906px]" :src="imgDevices" alt="imgDevices" draggable="false">
      </div>
      <div class=" flex flex-col gap-[90px] DTL:gap-[72px] mb-[130px] DTL:mb-[150px]">
        <div class=" flex flex-col gap-[11px] DTL:gap-5 text-center">
          <h2
            class=" text-neo-dark-blue text-[28px] DTL:text-[36px] leading-[35px] DTL:leading-[45px] tracking-[-.46px] DTL:tracking-[-.59px] font-semibold">
            Supercharge your workflow
          </h2>
          <p class=" text-[16px] DTL:text-[18px] leading-[26px] DTL:leading-[30px] tracking-[.12px] DTL:tracking-[.14px]">
            We’ve got the tools to boost your productivity.
          </p>
        </div>
        <div class=" flex flex-col DTL:flex-row DTL:items-start gap-14 DTL:gap-[30px] TB:px-32 text-center">
          <FeaturesTwo dataIndex="0" DTLGap="DTL:gap-10" />
          <FeaturesTwo dataIndex="1" DTLpaddingT="DTL:pt-1" />
          <FeaturesTwo dataIndex="2" DTLpaddingT="DTL:pt-1" />
        </div>
      </div>
      <div class=" flex flex-col DTL:flex-row items-center gap-14 DTL:gap-24 mb-[170px] DTL:mb-[150px]">
        <PartnersLogo :logoIndex="0" />
        <PartnersLogo :logoIndex="1" />
        <PartnersLogo :logoIndex="2" />
        <PartnersLogo :logoIndex="3" />
        <PartnersLogo :logoIndex="4" />
      </div>
      <div class=" flex flex-col gap-[46px] DTL:gap-12">
        <div class=" flex flex-col gap-4 DTL:gap-5 TB:px-12 DTL:px-80 text-center">
          <h2
            class=" text-neo-dark-blue text-[28px] DTL:text-[36px] leading-[35px] DTL:leading-[45px] tracking-[-.46px] DTL:tracking-[-.59px] font-semibold">
            Clipboard for iOS and Mac OS
          </h2>
          <p class=" text-[16px] DTL:text-[18px] leading-[26px] DTL:leading-[30px] tracking-[.12px] DTL:tracking-[.14px]">
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
    <footer
      class=" flex flex-col DTL:flex-row DTL:justify-center items-center gap-10 TB:gap-16 DTL:gap-[135px] w-full py-[52px] DTL:py-12 bg-neo-grayish-blue bg-opacity-10">
      <logo class=" scale-[.44] -m-[35px]" />
      <div class=" flex flex-col TB:flex-row items-center TB:items-start gap-12 TB:gap-24 DTL:gap-[165px]">
        <div
          class=" grid grid-flow-col grid-rows-5 TB:grid-rows-3 DTL:grid-rows-2 gap-5 DTL:gap-x-[30px] TB:gap-y-4 text-center TB:text-right DTL:text-left">
          <FooterText mainText="FAQs" />
          <FooterText mainText="Contact Us" />
          <FooterText mainText="Privacy Policy" />
          <FooterText mainText="Press Kit" />
          <FooterText mainText="Install Guide" />
        </div>
        <div class=" flex DTL:self-center gap-10 TB:gap-6">
          <NetworkIcon iconName="facebook" />
          <NetworkIcon iconName="twitter" />
          <NetworkIcon iconName="instagram" />
        </div>
      </div>
    </footer>
  </body>
</template>