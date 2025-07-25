<script setup lang="ts">
interface Props {
  
  label: string;
  modelValue: string | number;
  required: boolean;
  disabled?: boolean;
}

const props = withDefaults(defineProps<Props>(), {
  disabled: false,
});

const emit = defineEmits<{
  (e: "update:modelValue", value: string): void;
}>();

</script>
<template>
  <div>
    <div class="text-subtitle-1 text-medium-emphasis">Account</div>
    <v-text-field
      v-model="modelValue"
      density="compact"
      type="text"
      variant="outlined"
      :disabled="props.disabled"
      :required="true"
      hide-details="auto"
    ></v-text-field>
  </div>
</template>

<style scoped></style>
