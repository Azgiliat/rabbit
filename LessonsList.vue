<template>
  <ul class="lessons-list">
    <li class="lessons-list__item">
      <LessonCard class="lessons-list__lesson-card"
                  v-for="lesson in showedLessons" :key="lesson.id"
                  :title="lesson.title"
                  :description="lesson.description">
        <LessonImage slot="top"/>
      </LessonCard>
    </li>
  </ul>
</template>

<script>
import LessonCard from './LessonCard'
import LessonImage from './LessonImage'

export default {
  name: 'LessonsList',
  components: {
    LessonImage,
    LessonCard
  },
  props: {
    lessons: {
      type: Array,
      require: true
    },
    isFull: {
      type: Boolean,
      require: false,
      default: false
    }
  },
  computed: {
    showedLessons() {
      if (this.isFull) {
        return this.lessons
      }
      switch (this.$mq) {
        case 'modile':
          return this.lessons.slice(0, 2)
        default:
          return this.lessons.slice(0, 4)
      }
    }
  }
}
</script>

<style scoped>

</style>
