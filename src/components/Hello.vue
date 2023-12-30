<script setup>
import { ref, reactive } from "vue";
const count = ref(0);
const state = reactive({
  count: 1,
});

const addRefCount = () => {
  count.value++;
  state.count++;
};

const props = defineProps({
  msg: String,
});
</script>

<template>
  <h2>コンポーネント</h2>
  <p>count:{{ count }}</p>
  <p>state:{{ state.count }}</p>
  <div>
    <button @click="addRefCount">count++</button>
  </div>
  <p>{{ props.msg }}</p>
</template>
