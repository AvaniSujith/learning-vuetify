<script setup lang="ts">
const props = defineProps<{
    label:string,
    placeholder?: string,
    modelValue: string | number,

}>();
</script>
<template>
  <div>
    <div class="text-subtitle-1 text-medium-emphasis">Account</div>
    <v-text-field
      density="compact"
      placeholder="Email address"
      variant="outlined"
    ></v-text-field>
  </div>
</template>
<style scoped>

</style> 