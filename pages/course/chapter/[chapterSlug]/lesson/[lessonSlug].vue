<template>
  <h2>Lesson</h2>
  <p>{{chapter.title}}</p>
  <p>{{lesson.title}}</p>
</template>

<script setup>
const course = useCourse();
const route = useRoute();

const chapter = computed(() => course.chapters.find(chapter => chapter.slug === route.params.chapterSlug));
const lesson = computed(() => chapter.value.lessons.find(lesson => lesson.slug === route.params.lessonSlug));
console.log(chapter)
</script>