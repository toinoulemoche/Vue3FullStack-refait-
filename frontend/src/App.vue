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

</script>

<template>
	<DemoRef/>
</template>

<style></style>