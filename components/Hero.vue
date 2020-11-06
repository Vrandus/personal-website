<template> 
     <section class="hero is-info is-large">
          <div class="hero-body">
               <div class="container">
                    <h1 class="title">
                    {{ title }}
                    </h1>
                    <h2 class="subtitle">
                    {{ subtitle }}
                    </h2>
               </div>
          </div>
     </section>
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
     .hero{
          height: 60%;
          background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("../assets/hero-old.jpg");
          background-position: center;
          background-repeat: no-repeat;
          background-size: cover;
          position: relative;
     }
     .title {
          margin-left: 4rem;
          font-size: 4rem;
          filter: none;
          opacity: 80%;
     }
     .subtitle{
          margin-left: 6rem;
          opacity: 70%;
     }
     .hero-body {
          filter: none;
     }
</style>