<template>
  <div>
    {{ msg }}
    <h1 class="border-double border-4 border-indigo-600 w-2xl">哈哈</h1>
    <div ref="target" class="border-4">
      <h1>Hello world</h1>
      <p>x: {{ x }}</p>
      <p>y: {{ y }}</p>
      <p>isOutside: {{ isOutside }}</p>
    </div>
    <HelloWorld />
    <UserUserComponent />
    <el-row class="mt-4">
      <el-button>Default</el-button>
      <el-button type="primary">Primary</el-button>
      <el-button type="success">Success</el-button>
      <el-button type="info">Info</el-button>
      <el-button type="warning">Warning</el-button>
      <el-button type="danger">Danger</el-button>
    </el-row>
    <!-- A basic anchor icon from Phosphor icons -->
    <div class="i-ph-anchor-simple-thin" />
    <!-- An orange alarm from Material Design Icons -->
    <div class="i-mdi-alarm text-orange-400" />
    <!-- A large Vue logo -->
    <div class="i-logos-vue text-3xl" />
    <!-- Sun in light mode, Moon in dark mode, from Carbon -->
    <button class="i-carbon-sun dark:i-carbon-moon" />
    <!-- Twemoji of laugh, turns to tear on hovering -->
    <div class="i-twemoji-grinning-face-with-smiling-eyes hover:i-twemoji-face-with-tears-of-joy" />
    <div class="i-iconoir:4k-display text-8xl"></div>
  </div>
</template>

<script setup lang="ts">
const msg = ref('Hello World1')
const target = ref(null)
const { x, y, isOutside } = useMouseInElement(target)
</script>

<style scoped></style>

<route lang="yaml">
meta:
layout: default
</route>
