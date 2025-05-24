<template>
  <button
    v-if="colorMode.preference == 'dark'"
    @click="changeColorMode('light')"
    title="Light"
  >
    <Icon
      name="line-md:moon-filled-to-sunny-filled-loop-transition"
      style="width: 2rem"
    />
  </button>
  <button v-else @click="changeColorMode('dark')" title="Dark">
    <Icon
      name="line-md:sunny-filled-loop-to-moon-filled-alt-loop-transition"
      style="width: 2rem"
    />
  </button>
</template>

<script setup>
const colorMode = useColorMode();

function changeColorMode(mode) {
  colorMode.preference = mode;
}
</script>

<style lang="scss" scoped></style>
