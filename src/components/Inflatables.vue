<template>
  <section class="inflatables" id="Inflatables">
    <div class="container py-5">
      <h2 class="text-center font-weight-light mb-4">{{ sectionTitle }}</h2>
      <div class="row">
        <div class="col-xs-12 col-md-6 text-center inflatable mb-4 mb-md-0"
             v-for="inflatable in inflatables"
             :key="inflatable.title">
          <div :alt="inflatable.title"
               class="inflatable__image mb-2 mb-md-4"
               :style="{ backgroundImage: `url('${require(`../assets/images/${inflatable.image}`)}')` }">
          </div>
          <h5>{{ inflatable.title }}</h5>
          <p>{{ inflatable.description }}</p>
          <p class="mb-0"><i>{{ inflatable.rate }}</i> per hour</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    data () {
      return {
        inflatables: [
          {
            description: 'A jungle themed bounce castle with a detachable slide that can function wet or dry, perfect for any season!',
            image: 'placeholder.png',
            rate: '$100.00',
            title: 'Wet/Dry Jungle Slide Combo Unit'
          },
          {
            description: 'A 30 foot jungle obstacle course with a climbing wall, a slide, and many inflatable obstacles, great for all ages.',
            image: 'placeholder.png',
            rate: '$125.00',
            title: 'Jungle Obstacle Course'
          }
        ],
        sectionTitle: 'Inflatables'
      }
    }
  }
</script>

<style scoped lang="scss">
  @import '../sass/utils/variables';

  .inflatables {
    background-image: linear-gradient(to bottom right, lighten($red, 50%), $white);
  }

  .inflatable {
    &__image {
      background-position: center center;
      background-size: cover;
      border: .15rem solid $white;
      border-radius: 10px;
      max-height: 250px;
      min-height: 250px;
      width: 100%;
    }
  }
</style>