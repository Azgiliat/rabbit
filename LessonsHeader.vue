<template>
  <div class="lessons-header">
    <h4 class="lessons-header__title">
      {{ title }}
    </h4>
    <div class="lessons-header__nav" v-show="isFull">
      <router-link :to="to">
        Все уроки
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LessonsNav',
  props: {
    isFull: {
      type: Boolean,
      require: false,
      default: false
    },
    to: {
      type: String,
      require: false,
      default: ''
    },
    title: {
      type: String,
      require: true
    }
  }
}
</script>

<style scoped>

</style>
