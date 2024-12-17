<!-- eslint-disable vue/multi-word-component-names -->
<script setup lang="ts">
import { defineEmits } from 'vue'

import Branch from './List.vue'

const emit = defineEmits(['branch:click'])
</script>

<template>
  <Branch @branch:click="() => emit('branch:click')" />
</template>
