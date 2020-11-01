<template>
     <div>
      <div class="columns is-desktop">
        <div class="center column is-half-desktop">
          <h1>{{employer}}</h1>
          <slot/>
        </div>
        <div class="column is-half-desktop">
          <img class="amd-logo" src="logo">
        </div>
      </div>
    </div>
</template>

<script>
export default {
  props: {
    employer: {
      type: String,
      required: true,
    },
    logo: {
      type: String,
      required: true,
    },
    content: {
      type: String,
      required: true,
    }
  },
}
</script>


<style>
  .title {
    font-size: 1rem;
  }
    .amd-logo {
    height: 100%;
    width: 100%;
    border-radius: 100%;
    position: relative;
    padding: 6rem 6rem 6rem 6rem;
    
  }
</style>