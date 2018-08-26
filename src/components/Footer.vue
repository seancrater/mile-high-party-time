<template>
  <footer class="footer">
    <div class="container">
      <div class="row pt-3">
        <div class="col-9">
          <p>&copy; {{ currentYear }} Mile High Party Time LLC.</p>
        </div>
        <div class="col-3 footer__social">
          <Social />
        </div>
      </div>
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

<style scoped lang="scss">
  @import '../sass/utils/variables';

  .footer {
    border-top: .25rem solid $blue;
  }
</style>