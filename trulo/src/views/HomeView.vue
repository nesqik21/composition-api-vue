<template>
  <div>
    <button @click="score++" class="btn btn-green">{{ score }}</button>
    <p>Twice the score is: {{ double }}</p>
  </div>
</template>

<script>
import { ref, computed } from "vue";
export default {
  setup() {
    const score = ref(0);
    const double = computed(() => score.value * 2);
    return { score, double };
  },
};
</script>

<style lang="scss" scoped></style>
