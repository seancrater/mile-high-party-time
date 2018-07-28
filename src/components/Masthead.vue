<template>
  <section id="Masthead">
    <div class="container masthead text-center">
      <img :alt="title" src="../assets/logo.png">
      <p class="lead">{{leadText}}</p>
    </div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
      <div class="container">
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavDropdown">
          <ul class="navbar-nav">
            <li class="nav-item active" v-for="(value, key) in menuItems" :key="key">
              <a class="nav-link" :href="`#${key}`">{{ value }}</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </section>
</template>

<script>
  export default {
    data () {
      return {
        leadText: 'Rental bouncy castles and more!',
        menuItems: {
          Masthead: 'Home',
          AboutUs: 'About Us',
          Inflatables: 'Inflatables',
          ComingSoon: 'Coming Soon',
          ContactUs: 'Contact Us'
        },
        title: 'Mile High Party Time'
      }
    },
    mounted() {
      // TODO: Smooth scrollling script here
    }
  }
</script>
