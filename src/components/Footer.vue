<template>
  <footer>
    <div class="container">
      <p>&copy; {{ currentYear }} Mile High Party Time LLC.</p>
      <Social />
    </div>
  </footer>
</template>

<script>
  import Social from './Social.vue';

  export default {
    components: {
      Social
    },
    computed: {
      currentYear() {
        return new Date().getFullYear();
      }
    }
  };
</script>
