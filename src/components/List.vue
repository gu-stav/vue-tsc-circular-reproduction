<!-- eslint-disable vue/multi-word-component-names -->
<script setup lang="ts">
import { computed, defineEmits } from 'vue'

import { CollapsibleRoot } from 'radix-vue'

import Sublist from './Sublist.vue'

const emit = defineEmits(['branch:click'])
const isOpen = computed(() => true)
</script>

<template>
  <CollapsibleRoot v-model:open="isOpen" as-child>
    <Sublist @branch:click="() => emit('branch:click')" />
  </CollapsibleRoot>
</template>
