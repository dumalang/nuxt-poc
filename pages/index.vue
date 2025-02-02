<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        nuxt-poc
      </h1>
      <h2 class="subtitle">
        My cat&#39;s meow Nuxt.js project
      </h2>
      <div class="links">
        <input class="" type="text" v-model="userId"/>
        <button @click="onClickBtnUsers" class="button--green">LOAD USER</button>
      </div>
      <div class="links">
        <a
          href="/users/1000"
          target="_blank"
          class="button--green"
        >
          Go To User with ID 100
        </a>
        <nuxt-link to="/about-us" class="button--green">Go To About Us</nuxt-link>
      </div>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  data() {
    return {
      userId: 'defaultUserID'
    }
  },
  methods: {
    onClickBtnUsers() {
      alert('Users: ' + this.userId)
      this.$router.push(`/users/${this.userId}`)
    }
  },
  components: {
    Logo
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
