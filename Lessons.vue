<template>
  <div class="lessons">
    <div class="lessons__header">
      <slot name="header" />
    </div>
    <dil class="lessons__content">
      <slot name="content" />
    </dil>
  </div>
</template>

<script>
export default {
  name: 'Lessons'
}
</script>

<style scoped>

</style>
