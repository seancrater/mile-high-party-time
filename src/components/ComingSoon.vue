<template>
  <section id="ComingSoon">
    <div class="container py-5">
      <h2 class="text-center font-weight-light">{{ sectionTitle }}</h2>
      <h6 class="text-center">These are some of the other wonderful party options we will be offering in the near future!</h6>
      <div class="row">
        <div
          class="col-xs-6 col-md-3 mt-4"
          v-for="attraction in attractions"
          :key="attraction.name">
          <div
            class="coming-soon__image"
            :style="{ backgroundImage: `url('${require(`../assets/images/coming-soon/${attraction.image}`)}')` }"></div>  
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      attractions: [
        {
          image: 'photo-booth.jpg',
          name: 'Photo Booths'
        },
        {
          image: 'rock-climbing-wall.jpg',
          name: 'Rock Wall'
        },
        {
          image: 'velcro-wall.jpg',
          name: 'Velcro Wall'
        },
        {
          image: 'cotton-candy.jpg',
          name: 'Cotton Candy'
        }
      ],
      sectionTitle: 'Coming Soon',
      subtitle: 'These are some of the other wonderful party options we will be offering in the near future!'
    }
  }
}
</script>

<style lang="scss">
  @import '../sass/utils/variables';

  .coming-soon {
    &__image {
      background-position: center center;
      background-size: cover;
      border: .15rem solid $white;
      border-radius: 10px;
      max-height: 250px;
      min-height: 250px;
    }
  }
</style>