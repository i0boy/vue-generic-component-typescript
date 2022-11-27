<script setup lang="ts">
import { ButtonHTMLAttributes } from "vue";
interface Props extends ButtonHTMLAttributes {
  msg?: string;
  count?: string;
}
defineProps<Props>();
</script>
<script lang="ts">
export default {
  inheritAttrs: false,
};
</script>
<template>
  <h1>{{ msg }}</h1>
  <div class="card">
    <button type="button" v-bind="$attrs">
      at Children {{ count || "1" }}
    </button>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
