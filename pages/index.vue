<template>
  <section class="section">
    <About title="About Me" id="about">
      Raised in the suburbs of Toronto, I'm a 4th year York University student 
      currently studying Computer Science. 
    </About>
    <h1 class="work">
      Work Experience
    </h1>
    <Work v-for="experience in experiences"
    v-bind="experience.employer"
    >
      {{experience.content}}
    </Work>
    <div class="columns is-desktop">

      <card title="Free" icon="linkedin">
        Open source on <a href="https://github.com/buefy/buefy"> GitHub </a>
      </card>

      <card title="Responsive" icon="cellphone-link">
        <b class="has-text-grey"> Every </b> component is responsive
      </card>

      <card title="Modern" icon="alert-decagram">
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
          logo : "../assets/amd-red.png",
          content: "",
          isLeft: false
        },
        {
          employer : "Jupio Labs",
          logo : "",
          content : "",
          isLeft: true
        },
        {
          employer : "York University",
          logo : "",
          content : "",
          isLeft: false
        }
      ]
    }
  }
}
</script>

<style>
  .work {
    margin: auto;
    text-align: center;
  }
</style>