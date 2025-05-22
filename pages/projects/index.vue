<template>
  <div class="grid grid-cols-3 gap-4 my-4">
    <projectCard v-for="project in data" :project="project" :key="project.id" />
  </div>
</template>

<script setup>
const { data, error, loading } = useFetch(
  "https://api.github.com/users/yousef-mostafa/repos"
);
</script>

<style lang="scss" scoped></style>
