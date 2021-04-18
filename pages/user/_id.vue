<template>
  <div>
    <span>Profile {{ $route.params.id }}</span>
  </div>
</template>

<script>
export default {
  validate({ params }) {
    //must be a number
    return /^\d+$/.test(params.id);
  }
};
</script>

<style lang="scss" scoped></style>
