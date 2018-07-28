<template>
  <section class="masthead" id="Masthead">
    <div class="container text-center py-4">
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
            <li class="nav-item" v-for="(value, key) in menuItems" :key="key" :class="{ active: activeLink === key }">
              <a class="nav-link" @click="route(key)" href="javascript:void(0)">{{ value }}</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </section>
</template>

<script>
  export default {
    data() {
      return {
        activeLink: 'Masthead',
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
    methods: {
      route(newRoute) {
        this.activeLink = newRoute;
        this.scrollTo(newRoute);
      },
      scrollTo(elementID) {
        const targetElement = document.getElementById(elementID);
        console.log(targetElement);
      }
    },
    mounted() {
      // TODO: Smooth scrollling script here
    }
  }
</script>

<style scoped>
  .masthead {
    background: linear-gradient(rgba(255,255,255,0.75), rgba(155,155,155,.75)),url('../assets/images/background.jpg');
  }
</style>
