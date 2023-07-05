<template>
  <div>
    <button @click="score++" class="btn btn-green">{{ score }}</button>
    <p>Twice the score is: {{ double }}</p>
    <br />
    <p>My name is: {{ myNameIs }}</p>
  </div>
</template>

<script>
import { reactive, toRefs } from "vue";
export default {
  setup() {
    const state = reactive({
      score: 0,
      myNameIs: "Tomas",
    });
    return { ...toRefs(state) };
  },
};
</script>

<style lang="scss" scoped></style>
