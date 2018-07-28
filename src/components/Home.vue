<template>
  <Masthead />
</template>

<script>
import AboutUs from './AboutUs.vue';
import ComingSoon from './ComingSoon.vue';
import Inflatables from './Inflatables.vue';
import Masthead from './Masthead.vue';

export default {
  name: 'home',
  components: {
    AboutUs,
    ComingSoon,
    Inflatables,
    Masthead
  }
}
</script>