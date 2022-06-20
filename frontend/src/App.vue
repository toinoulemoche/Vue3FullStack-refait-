<script setup>
import { useRouter, useRoute } from 'vue-router'

const router = VueRouter.createRouter({
history: VueRouter.createWebHistory(),
routes: [
    {
    path: '/',
    name: 'Home',
    component: Home
    },
    {
    path: '/about',
    name: 'About',
    component: About
    },
    {
    path: '/login',
    name: 'Login',
    component: Login
    },
    {
    path: '/register',
    name: 'Register',
    component: Register
    },
    {
    path: '/todo',
    name: 'Todo',
    component: Todo
    }
  ]
})

new Vue({
  el: '#register',
  data () {
    return {
      info: null
    }
  },
  mounted () {
    axios
      .get('mongodb+srv://toinou:<password>@cluster0.qmdph.mongodb.net/?retryWrites=true&w=majority')
      .then(response => (this.info = response))
  }
})

new Vue({
  el: '#login',
  data () {
    return {
      jwt: null
    }
  },
  mounted () {
    axios
      .get('mongodb+srv://toinou:<password>@cluster0.qmdph.mongodb.net/?retryWrites=true&w=majority')
      .then(response => (this.jwt = response))
  }
})

</script>

<template>
	<DemoRef/>
</template>

<style></style>