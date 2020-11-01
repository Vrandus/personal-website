<template>
     <div class="card">
      <div v-if="employer.isFlipped">
        <div class="columns is-desktop">
          <div class="center column is-half-desktop">
            <h1>{{employer.employer}}</h1>
            <h2 class="work-title">{{employer.title}}</h2>
            <h2 class="work-title">{{employer.dates}}</h2>
            <p class="work-content">{{employer.content}}</p>
          </div>
          <div class="column is-half-desktop">
            <img class="amd-logo" :src="employer.logo">
          </div>
        </div>
      </div>
      <div v-else>
        <div class="columns is-desktop">
          <div class="column is-half-desktop">
            <img class="amd-logo" :src="employer.logo">
          </div>
          <div class="center column is-half-desktop">
            <h1>{{employer.employer}}</h1>
            <h2 class="work-title">{{employer.title}}</h2>
            <h2 class="work-title">{{employer.dates}}</h2>
            <p class="work-content">{{employer.content}}</p>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  props: {
    employer: {
      type: Object,
      required: true,
    },

  },
}
</script>


<style>
    .amd-logo {
    height: 100%;
    width: 100%;
    border-radius: 100%;
    position: relative;
    padding: 6rem 6rem 6rem 6rem;
    
  }
  .work-title {
    font-size: 1.3rem;
    opacity: 80%;
  }
  .work-content {
    padding-left: 4rem;
    padding-right: 4rem;
    padding-bottom: 2rem;
  }
</style>