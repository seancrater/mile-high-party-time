<template>
  <div class="home">
    <Masthead />
    <AboutUs />
    <Inflatables />
    <ComingSoon />
    <ContactUs />
    <Footer />
  </div>
</template>

<script>
import AboutUs from './AboutUs.vue';
import ComingSoon from './ComingSoon.vue';
import ContactUs from './ContactUs.vue';
import Footer from './Footer.vue';
import Inflatables from './Inflatables.vue';
import Masthead from './Masthead.vue';

export default {
  components: {
    AboutUs,
    ComingSoon,
    ContactUs,
    Footer,
    Inflatables,
    Masthead
  }
}
</script>