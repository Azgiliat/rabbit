<template>
  <img class="img" :src="url" />
</template>

<script>
export default {
  name: 'LessonImage',
  props: {
    url: {
      type: String,
      require: true
    }
  }
}
</script>
