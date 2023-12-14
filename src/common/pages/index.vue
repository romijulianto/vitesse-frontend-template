<script setup lang="ts">
// Routing
const router = useRouter()
const go = () => {
  router.push('/users/home')
}
</script>

<template>
  <div>
    <n-button type="warning" @click="go">
      click
    </n-button>
  </div>
</template>
