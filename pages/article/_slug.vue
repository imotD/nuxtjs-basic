<template>
  <div>
    <span></span>
    <main v-if="$route.params.slug">
      <p>Article {{ $route.params.slug }}</p>
    </main>
    <main v-else>
      <p>List Article</p>
    </main>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped></style>
