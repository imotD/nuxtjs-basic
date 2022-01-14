<template>
  <div>
    {{ $route.params.slug }}
    <pre>
      {{ $data }}
    </pre>
  </div>
</template>

<script>
export default {
  async asyncData() {
    const planet = await fetch(
      `https://api.nuxtjs.dev/planets/${params.slug}`
    ).then((res) => {
      if (res.ok) {
        return res.json();
      }
      throw new Error(res.status);
    });
    return { planet };
  },
};
</script>

<style lang="scss" scoped></style>
