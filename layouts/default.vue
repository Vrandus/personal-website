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
            <b-navbar-item href="/11-26-2021-resume.pdf">
                Resume
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
      <Hero title="Prateek Tailor" subtitle="Software Engineer, Photographer"/>
      <div class="container column is-10">
        <nuxt />
      </div>
            <SplitHero      
              title="Photography" subtitle="I love photography, from portraits to landscapes. I've been taking photos for a couple years now and have had some paid gigs. All the photos on this website were taken by me, visit my Instagram linked below for more! "
              titles="Gunpla"  subtitles="Not a typo! Gunpla stands for Gundam + Plastic model. As a kid, I was always into giant mechs like Transformers and that obsession eventually led to learning about Gundams. I've been building Gunpla kits since."/>
    </section>
    <footer class="footer">
      <div class="content has-text-centered">
        <p>
          <strong>Find Me On</strong>
          <div>
            <a href="https://www.linkedin.com/in/prtailor/" target="_blank"><b-icon :icon="linkedin" size="is-large" type="is-primary"/></a>
            <a href="https://github.com/vrandus" target="_blank"><b-icon :icon="github" size="is-large" type="is-primary"/></a>
            <a href="https://www.instagram.com/prateektailor/" target="_blank"><b-icon :icon="instagram" size="is-large" type="is-primary"/></a>
          </div>
        </p>
      </div>
    </footer>
  </div>
</template>

<script>
import About from '~/components/About' 
import Hero from '~/components/Hero'
import SplitHero from '~/components/Split-Hero'
export default {
    components: {
    Hero,
    About,
    SplitHero
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