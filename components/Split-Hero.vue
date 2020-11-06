<template> 
     <section class="columns">
          <section class=" column hero hero1 is-info is-large">
               <div class="hero-body">
                    <div class="container">
                         <h1 class="titles title">
                         {{ title }}
                         </h1>
                         <h2 class="subtitles subtitle">
                         {{ subtitle }}
                         </h2>
                    </div>
               </div>
          </section>
          <section class=" column hero hero2 is-info is-large">
               <div class="hero-body">
                    <div class="container">
                         <h1 class="titles title">
                         {{ titles }}
                         </h1>
                         <h2 class="subtitles subtitle">
                         {{ subtitles }}
                         </h2>
                    </div>
               </div>
          </section>
     </section>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
     titles: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
     subtitles: {
      type: String,
      required: true,
    },
  },
}
</script>

<style>
     .hero1{
          height: 50%;
          background-image: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.5)), url("../assets/hobbies1.jpg");
          background-position: center;
          background-repeat: no-repeat;
          background-size: cover;
          position: relative;
     }
     .hero2{
          height: 50%;
          background-image: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.5)), url("../assets/hobbies2.jpg");
          background-position: center;
          background-repeat: no-repeat;
          background-size: cover;
          position: relative;
     }
     .titles {
          text-align: center;
          font-size: 4rem;
          opacity: 0.8;
     }
     .subtitles{
          text-align: center;
          padding: 0 1rem;
          opacity: 0.7;
     }
     .hero-body {
          filter: none;
     }
</style>