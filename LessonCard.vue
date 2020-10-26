<template>
  <div class="lesson-card">
    <div class="lesson-card__top">
      <slot name="top"/>
    </div>
    <p class="lesson-card__title">
      {{ title }}
    </p>
    <p class="lesson-card__description">
      {{ description }}
    </p>
  </div>
</template>

<script>
export default {
  name: 'LessonCard',
  props: {
    title: {
      type: String,
      require: true
    },
    description: {
      type: String,
      require: false,
      default: ''
    }
  }
}
</script>

<style scoped>

</style>
