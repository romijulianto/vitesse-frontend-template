<script setup lang="ts">
// Routing
const router = useRouter()
const go = () => {
  router.push('/users/home')
}
</script>

<template>
  <div>
    <div class="py-4" />

    <div>
      <button
        class="m-3 text-sm btn"
        @click="go"
      >
        click here
      </button>
    </div>
  </div>
</template>
