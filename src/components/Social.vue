<template>
  <div class="social-icons" :class="modifierClass">
    <a v-for="(platformUrl, platformName, index) in socialPlatforms"
       :class="{ 'mr-2': index === 0 }"
       :key="platformName" :href="platformUrl"
       rel="noopener noreferrer"
       target="_blank">
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
