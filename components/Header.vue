<template>
  <nav class="flex justify-between py-8">
    <!-- logo -->
    <div class="text-text-primary font-bold text-2xl">
      <NuxtLink to="/" class="link-hover"> Yousef </NuxtLink>
    </div>

    <ul class="flex gap-5 text-lg font-medium">
      <li><NuxtLink to="/" class="link-hover"> Main</NuxtLink></li>
      <li><NuxtLink to="about" class="link-hover"> About</NuxtLink></li>
      <li><NuxtLink to="projects" class="link-hover"> Projects</NuxtLink></li>
    </ul>

    <!-- theme switcher -->
    <ClientOnly>
      <ThemeSwitcher />
    </ClientOnly>
  </nav>
</template>

<script setup></script>

<style lang="scss" scoped>
.link-hover {
  @apply hover:text-primary;
  transition: color 0.3s ease-in-out;
}
</style>
