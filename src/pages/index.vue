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
  </div>
</template>

<script setup lang="ts">
const msg = ref('Hello World1')
const target = ref(null)
const { x, y, isOutside } = useMouseInElement(target)
</script>

<style scoped></style>
