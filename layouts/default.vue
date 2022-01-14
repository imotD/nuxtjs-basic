<template>
  <div>
    <div v-if="$nuxt.isOffline">You are offline</div>
    <div v-if="$nuxt.isOnline">
      <Nuxt />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped></style>
