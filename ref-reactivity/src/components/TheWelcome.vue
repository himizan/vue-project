<script setup>
import { ref } from "vue";

const obj = ref({
  name: "Mitu",
  age: 21,
});

setTimeout(() => {
  console.log("set time out call");
  console.log("obj", obj);
  console.log("obj.name.value", obj.name);
  console.log("obj.value", obj.value);
  console.log("obj.age.value", obj.age);
}, 2000);

let count = ref(0);

const increment = () => {
  count.value++;
};
const decrement = () => {
  if (count.value <= 0) return;
  count.value--;
};
</script>

<template>
  <div>
    <h1>{{ obj.name }}</h1>
    <h2>{{ obj.age }}</h2>
    <h2>{{ count }}</h2>
    <button @click="increment">Increment</button>
    <button @click="decrement">Decrement</button>
  </div>
</template>
