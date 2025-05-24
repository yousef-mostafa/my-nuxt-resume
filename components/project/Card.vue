<template>
  <div
    class="border border-background-secondary rounded-lg p-4 dark:bg-background-secondary"
  >
    <!-- header -->
    <div class="flex justify-between items-center mb-4">
      <a
        class="font-bold flex gap-1 items-center text-text-primary"
        :href="project.html_url"
        target="_blank"
      >
        {{ project.name }}
        <Icon name="flowbite:arrow-up-right-from-square-outline"></Icon>
      </a>
      <div
        v-if="project.fork"
        class="border rounded p-2 text-green-800 dark:text-green-400 shrink-0 font-bold flex items-center gap-1"
      >
        <Icon name="tabler:arrow-fork"></Icon> Forked
      </div>
    </div>
    <!-- description -->
    <div class="text-text-secondary">
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
