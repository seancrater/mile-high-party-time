<template>
  <section class="contact-us" id="ContactUs">
    <div class="container text-center py-5">
      <h2 class="font-weight-light mb-4">{{ sectionTitle }}</h2>
      <p>Interested in scheduling a rental? We'd love to hear from you!</p>
      <div class="contact-us__buttons">
        <a class="btn btn-info" href="tel:" rel="noopener noreferrer">Call us to schedule</a>
        <i class="mx-1">or</i>
        <a class="btn btn-primary" rel="noopener noreferrer">Email us</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      sectionTitle: 'Contact Us'
    }
  }
}
</script>

<style scoped lang="scss">
  @import '../sass/utils/variables';

  .contact-us {
    background-image: linear-gradient(to top left, lighten($blue, 65%), $white);

    &__buttons {
      color: $white;

      & i {
        color: $blue;
      }
    }
  }
</style>