<template>
  <div>
    <b-navbar fixed-top>
        <template slot="brand">
            <b-navbar-item class="name" tag="router-link" :to="{ path: '/' }">
              <div class="myName">Prateek <span class="col">Tailor</span></div>
            </b-navbar-item>
        </template>
        <template slot="start">
            <b-navbar-item href="#about">
                About Me
            </b-navbar-item>
            <b-navbar-item href="#work-experience">
                Work Experience
            </b-navbar-item>
            <b-navbar-item href="#projects">
                Projects
            </b-navbar-item>
            <b-navbar-item href="#hobbies">
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
    color: #7957d5;
  }
  .myName {
    font-Size: 1.5rem;
    font-weight: 500;
  }
  .name{
    margin-left: 5rem;
  }
</style>