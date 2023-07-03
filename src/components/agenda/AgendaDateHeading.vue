<template>
  <div
    class="flex py-1 border border-b-0 bg-custom-gray-800 justify-center w-full"
    :class="dateHeadingBorderClass"
  >
    <div class="flex-grow py-1 my-1 border-t border-b border-r" :class="dateHeadingDecorateClass">
      <div class="border-t border-b h-6px" :class="dateHeadingDecorateClass"></div>
    </div>
    <p class="mx-3 font-medium" :class="dateHeadingTextClass"><slot></slot></p>
    <div class="flex-grow py-1 my-1 border-t border-b border-l" :class="dateHeadingDecorateClass">
      <div class="border-t border-b h-6px" :class="dateHeadingDecorateClass"></div>
    </div>
  </div>
</template>

<script setup>
import { defineProps, computed } from "vue";

const props = defineProps({
  isActive: {
    type: Boolean,
  },
  isRight: {
    type: Boolean,
  },
});

const dateHeadingBorderClass = computed(() => ({
  "border-custom-teal-500": props.isActive,
  "border-custom-teal-700": !props.isActive,
  "border-l-0": props.isRight && !props.isActive,
  "border-r-0": !props.isRight && !props.isActive,
}));

const dateHeadingDecorateClass = computed(() => ({
  "border-custom-teal-500": props.isActive,
  "border-custom-teal-700": !props.isActive,
  invisible: !props.isActive,
}));

const dateHeadingTextClass = computed(() => ({
  "text-custom-teal-500": props.isActive,
  "text-custom-teal-700": !props.isActive,
}));
</script>
