<template>
  <div>
    <button @click="score++" class="btn btn-green">{{ score }}</button>
    <p>Twice the score is: {{ doubleTheScore }}</p>
    <br />
    <p>My name is: {{ myNameIs }}</p>
  </div>
</template>

<script>
import { reactive, toRefs, computed, onMounted } from "vue";
export default {
  setup() {
    const state = reactive({
      score: 0,
      myNameIs: "Tomas",
      doubleTheScore: computed(() => state.score * 2),
    });
    onMounted(() => alert("I AM READY"));
    return { ...toRefs(state) };
  },
};
</script>

<style lang="scss" scoped></style>
