<template>
  <div>
    <Masthead />
    <AboutUs />
    <Inflatables />
    <ComingSoon />
    <ContactUs />
  </div>
</template>

<script>
import AboutUs from './AboutUs.vue';
import ComingSoon from './ComingSoon.vue';
import ContactUs from './ContactUs.vue';
import Inflatables from './Inflatables.vue';
import Masthead from './Masthead.vue';

export default {
  components: {
    AboutUs,
    ComingSoon,
    Inflatables,
    Masthead
  }
}
</script>