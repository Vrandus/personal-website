<template>
  <section class="section">
    <About title="About Me" id="about">
      Raised in the suburbs of Toronto, I'm a 4th year York University student 
      currently studying Computer Science. 
      Mauris diam sem, dignissim id fermentum eu, laoreet eu tellus. Cras quis augue eu metus luctus fermentum in a tortor. 
    </About>
    <h1 class="work" id="work-experience">
      Work Experience
    </h1>
    <Work
    v-for="experience in experiences"
    :key="experience.employer"
    :employer="experience"
    />
    <div class="columns is-desktop">

      <card title="Free" icon="discord">
        Open source on <a href="https://github.com/buefy/buefy"> GitHub </a>
      </card>

      <card title="Responsive" icon="layers">
        <b class="has-text-grey"> Every </b> component is responsive
      </card>

      <card title="Modern" icon="folder-outline">
        Built with <a href="https://vuejs.org/"> Vue.js </a> and
        <a href="http://bulma.io/"> Bulma </a>
      </card>

      <card title="Lightweight" icon="arrange-bring-to-front">
        No other internal dependency
      </card>
    </div>
  </section>
</template>

<script>
import Card from '~/components/Card'
import Hero from '~/components/Hero'
import About from  '~/components/About'
import Work from '~/components/Work'
export default {
  name: 'HomePage',

  components: {
    Card,
    Hero
  },
  data() {
    return{
      experiences : [
        {
          employer : "AMD",
          title: "Software QA Engineer Intern",
          logo : "/amd-red.png",
          dates : "October 2020 - Present",
          content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut aliquet tellus ante, sit amet sodales massa ultricies quis. Curabitur bibendum aliquam erat, vel egestas elit dictum id. Mauris diam sem, dignissim id fermentum eu, laoreet eu tellus. Cras quis augue eu metus luctus fermentum in a tortor. Sed quis nibh quis tortor congue molestie. Donec ullamcorper enim massa, eu vehicula libero scelerisque vitae. Vestibulum mattis posuere magna et pulvinar. Curabitur dolor mauris, hendrerit sed dui eget, efficitur malesuada tortor. Phasellus congue maximus consectetur.",
          isFlipped: true
        },
        {
          employer : "Jupio Labs",
          title: "Software Engineer Intern",
          logo : "/jupio.png",
          dates : "September 2018 - January 2019",
          content : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut aliquet tellus ante, sit amet sodales massa ultricies quis. Curabitur bibendum aliquam erat, vel egestas elit dictum id. Mauris diam sem, dignissim id fermentum eu, laoreet eu tellus. Cras quis augue eu metus luctus fermentum in a tortor. Sed quis nibh quis tortor congue molestie. Donec ullamcorper enim massa, eu vehicula libero scelerisque vitae. Vestibulum mattis posuere magna et pulvinar. Curabitur dolor mauris, hendrerit sed dui eget, efficitur malesuada tortor. Phasellus congue maximus consectetur.",
          isFlipped: false
        },
        {
          employer : "York University",
          title: "Computing Support Assistant",
          logo : "/york.jpg",
          dates : "October 2017 - Present",
          content : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut aliquet tellus ante, sit amet sodales massa ultricies quis. Curabitur bibendum aliquam erat, vel egestas elit dictum id. Mauris diam sem, dignissim id fermentum eu, laoreet eu tellus. Cras quis augue eu metus luctus fermentum in a tortor. Sed quis nibh quis tortor congue molestie. Donec ullamcorper enim massa, eu vehicula libero scelerisque vitae. Vestibulum mattis posuere magna et pulvinar. Curabitur dolor mauris, hendrerit sed dui eget, efficitur malesuada tortor. Phasellus congue maximus consectetur.",
          isFlipped: true
        }
      ]
    }
  }
}
</script>

<style>
  #about {
    font-size: 1.2rem;
  }
  .work {
    margin: 1rem auto;
    text-align: center;
  }
</style>