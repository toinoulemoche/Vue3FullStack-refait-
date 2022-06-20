<script setup>
import { useRouter, useRoute } from 'vue-router'

export default {
  setup() {
    const router = useRouter()
    const route = useRoute()
    router.push({name: 'login', name: 'register'})
    }
}

</script>

<template>
	<DemoRef/>
</template>

<style></style>