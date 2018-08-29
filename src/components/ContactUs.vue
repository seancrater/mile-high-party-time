<template>
  <section class="contact-us" id="ContactUs">
    <div class="container text-center py-5">
      <h2 class="font-weight-light mb-4">{{ sectionTitle }}</h2>
      <p>Interested in scheduling a rental? We'd love to hear from you!</p>
      <div class="contact-us__buttons">
        <a href="tel:8027354949" rel="noopener noreferrer">Call us at 802-735-4949</a>
        <i class="mx-1">or</i>
        <a class="btn btn-primary" href="mailto:info@milehighpartytime.com" rel="noopener noreferrer">Email us</a>
        <span class="ml-1">to schedule</span>
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

      & i,
      & span {
        color: $blue;
      }
    }
  }
</style>