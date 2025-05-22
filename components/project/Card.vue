<template>
  <div class="bg-white rounded-lg shadow p-4">
    <!-- header -->
    <div class="flex justify-between items-center mb-4">
      <a class="font-bold flex gap-1 items-center" :href="project.html_url">
        {{ project.name }}
        <Icon name="flowbite:arrow-up-right-from-square-outline"></Icon>
      </a>
      <div
        v-if="project.fork"
        class="border rounded p-2 text-green-800 shrink-0 font-bold flex items-center gap-1"
      >
        <Icon name="tabler:arrow-fork"></Icon> Forked
      </div>
    </div>
    <!-- description -->
    <div class="text-gray-500">
      {{ project.description || "---" }}
    </div>
  </div>
</template>

<script setup>
const { project } = defineProps({
  project: {
    type: Object,
    default: () => {},
  },
});
</script>

<style lang="scss" scoped>
.truncate {
  overflow: hidden;
  text-overflow: ellipsis;
}
a {
  transition: 0.3s color ease-in-out;
  &:hover {
    @apply text-primary;
  }
}
</style>
