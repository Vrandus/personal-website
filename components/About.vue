<template>
    <div>
      <div class="columns is-desktop">
        <div class="column is-half-desktop">
          <img class="photo" src="../assets/me.jpg">
        </div>
        <div class="center column is-half-desktop">
          <h1>{{title}}</h1>
          <slot/>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
  },
}
</script>
<style>
  h1 {
    font-size: 2rem;
  }
  .name {
    font-size: 1rem;
  }
  .photo {
    height: 100%;
    width: 100%;
    border-radius: 100%;
    position: relative;
    padding: 4rem 4rem 4rem 4rem;
    
  }
  .center{
    margin: auto;
    text-align: center;
    @media screen and (min-width: $desktop;) {
      text-align:left;
    }
  }
</style>