<template>
  <section class="main">
    <ul class="main__list">
      <li class="main__list-item" v-for="lesson in lessons" :key="lesson.id">
        <Lessons>
          <LessonsHeader slot="header" :to="lesson.to" :title="lesson.title" :isFull="true"/>
          <LessonsList slot="content" :lessons="lesson.lessonsList"/>
        </Lessons>
      </li>
    </ul>
  </section>
</template>

<script>
import LessonsList from '../LessonsList'
import LessonsHeader from '../LessonsHeader'
import Lessons from '../Lessons'

export default {
  name: 'Main',
  components: {
    Lessons,
    LessonsHeader,
    LessonsList
  },
  data () {
    return {
      lessons: [
        {
          id: 0,
          title: 'Персональный бренд',
          to: '/lessons/personal-brand',
          lessonsList: []
        },
        {
          id: 42,
          title: 'Food Film',
          to: '/lessons/food-film',
          lessonsList: []
        }
      ]
    }
  }
}
</script>
