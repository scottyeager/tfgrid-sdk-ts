<template>
  <v-tooltip :text="tooltip" location="bottom">
    <template #activator="{ props }">
      <v-btn
        @click.stop="$emit('click', $event)"
        :icon="icon"
        :color="color"
        v-bind="props"
        :href="href"
        :target="href ? '_blank' : undefined"
        :height="height"
      />
    </template>
  </v-tooltip>
</template>

<script lang="ts" setup>
defineProps<{
  tooltip: string;
  icon: `mdi-${string}`;
  color?: string;
  href?: string;
  height?: string;
}>();
defineEmits(["click"]);
</script>

<script lang="ts">
export default {
  name: "IconActionBtn",
};
</script>
