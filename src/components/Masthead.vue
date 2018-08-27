<template>
  <section id="Masthead">
    <div class="masthead">
      <div class="container text-center py-4">
        <h1>
          <img :alt="title" src="../assets/logo.png">
          <span class="d-none">Mile High Party Time - Bouncy Castles in the Denver, Colorado Area</span>
        </h1>
        
        <p class="lead">{{leadText}}</p>
        <Social modifier-class="masthead__social" />
      </div>
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
  import Social from './Social.vue';

  export default {
    components: {
      Social
    },
    data() {
      return {
        activeLink: 'Masthead',
        leadText: 'Rental bouncy castles and more!',
        mastheadHeight: 0,
        menuFixed: false,
        menuHeight: 0,
        menuItems: {
          AboutUs: 'About Us',
          Inflatables: 'Inflatables',
          ComingSoon: 'Coming Soon',
          ContactUs: 'Contact Us'
        },
        title: 'Mile High Party Time'
      }
    },
    methods: {
      handleMenuPosition() {
        if (window.scrollY > this.mastheadHeight) {
          this.menuFixed = true;
        } else {
          this.menuFixed = false;
        }
      },
      route(newRoute) {
        this.activeLink = newRoute;
        this.scrollTo(newRoute);
      },
      scrollEvents() {
        this.handleMenuPosition();
        this.setActiveSection();
      },
      scrollTo(elementID) {
        const targetElement = document.getElementById(elementID);
        window.scroll({top: targetElement.offsetTop, left: 0, behavior: 'smooth' });
      },
      setActiveSection() {
        let sections = [...document.querySelectorAll('.home > section')];
        const currentScrollY = window.scrollY + this.menuHeight;

        sections = sections.filter(section => {
          if (section.getBoundingClientRect().top < currentScrollY) {
            return true;
          }
        });

        this.activeLink = sections[sections.length - 1].getAttribute('id');
      }
    },
    mounted() {
      this.mastheadHeight = document.querySelector('#Masthead').offsetHeight;
      this.menuHeight = document.querySelector('.navbar').offsetHeight;
      window.onscroll = this.scrollEvents;
    }
  }
</script>

<style lang="scss" scoped>
  .masthead {
    background: linear-gradient(rgba(255,255,255,0.75), rgba(194, 32, 47,.95)),url('../assets/images/background.jpg');
    background-size: cover;
    
    .container {
      position: relative;
    }

    &__social {
      display: inline-block;
      position: absolute;
      right: 1rem;
      top: 1.5rem;
    }
  }
</style>
