<template>
  <div>
    <b-navbar fixed-top>
        <template slot="brand">
            <b-navbar-item class="name" tag="router-link" :to="{ path: '/' }">
              <div class="myName">Prateek Tailor</div>
            </b-navbar-item>
        </template>
        <template slot="start">
            <b-navbar-item href="#about">
                About Me
            </b-navbar-item>
            <b-navbar-item href="#">
                Work Experience
            </b-navbar-item>
            <b-navbar-item href="#">
                Projects
            </b-navbar-item>
            <b-navbar-item href="#">
                Hobbies
            </b-navbar-item>
        </template>
        <template slot="end">
            <b-navbar-item href="https://www.linkedin.com/in/prtailor/" target="_blank" class="col">
                <b-icon :icon="linkedin" size="is-large" type="is-primary" />
            </b-navbar-item>
            <b-navbar-item href="https://github.com/vrandus" target="_blank">
                <b-icon :icon="github" size="is-large" type="is-primary"/>
            </b-navbar-item>
            <b-navbar-item href="https://www.instagram.com/prateektailor/" target="_blank">
                <b-icon :icon="instagram" size="is-large" type="is-primary"/>
            </b-navbar-item>
        </template>
    </b-navbar>
      <Hero title="Prateek Tailor" subtitle="Software Developer, Photographer"/>
      <div class="container column is-10">
        <nuxt />
      </div>
    </section>
  </div>
</template>

<script>
import About from '~/components/About' 
import Hero from '~/components/Hero'
export default {
    components: {
    Hero,
    About
  },
  data() {
    return {
      linkedin: "linkedin",
      github: "github",
      instagram: "instagram",
      items: [
        
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' },
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' },
        },
      ],
    }
  },
}
</script>
<style>
  .col {
    color: #00796B;
  }
  .myName {
    font-Size: 1.5rem;
    color: #00796B;
  }
  .name{
    margin-left: 5rem;
  }
</style>