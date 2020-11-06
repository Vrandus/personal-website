<template>
  
  <div class="column">
    <a :href="link" target="_blank">
    <div class="card box">
      <header class="card-header">
        <p class="c-title card-header-title has-text-grey has-text-centered">
          {{ title }}
        </p>
      </header>
      <div class="card-content">
        <div class="content has-text-centered">
          <b-icon :icon="icon" size="is-large" type="is-primary" />
        </div>
      </div>
      <footer class="card-footer">
        <div class="card-footer-item">
          <span>
            <slot />
          </span>
        </div>
      </footer>
    </div>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      required: true,
    },
    link: {
      type: String,
      required: false,
    }
  },
}
</script>
<style>
  .c-title {
    margin: 0 auto;
    text-align: center;
  }
  .card-footer-item {
    margin: 1rem 2rem;
  }
.box {
  transition: box-shadow .3s;
  
}
.box:hover {
  box-shadow: 0 0 11px rgba(33,33,33,.2); 
}
</style>