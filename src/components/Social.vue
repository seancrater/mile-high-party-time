<template>
  <div class="social-icons" :class="modifierClass">
    <a v-for="(platformUrl, platformName) in socialPlatforms" :key="platformName" :href="platformUrl" target="_blank">
      <img :alt="platformName" :src="platformIcons[platformName]" />
    </a>
  </div>
</template>

<script>
  import facebookIcon from '../assets/icons/facebook.svg';
  import instagramIcon from '../assets/icons/instagram.svg';

  export default {
    props: {
      modifierClass: {
        default: '',
        type: String
      }
    },
    data() {
      return {
        platformIcons: {
          facebook: facebookIcon,
          instagram: instagramIcon
        },
        socialPlatforms: {
          facebook: 'https://www.facebook.com/milehighpartytime/ ',
          instagram: 'https://www.instagram.com/mile_high_party_time'
        }
      }
    }
  };
</script>
