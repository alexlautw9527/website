<template>
  <div class="h-full flex flex-col justify-between">
    <div>
      <h2 class="text-white text-lg mb-2 leading-none">
        從 Domain-Driven Design 看網站開發框架隱藏
      </h2>
      <CategoryTag :tag="tag" />
    </div>

    <div class="flex items-center gap-2">
      <div class="rounded-full h-10 w-10 bg-white"></div>
      <h3 class="text-custom-pink-700">Ruddy 老師</h3>
    </div>
  </div>
</template>

<script setup>
import CategoryTag from "../CategoryTag.vue";

const tag = "前端";
</script>

<style lang="scss" scoped></style>
