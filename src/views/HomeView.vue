<template>
  <div class="home">
    Home
    <p ref="p">My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">Click</button>
  </div>
</template>

<script>
// @ is an alias to /src
import { ref } from "vue";

export default {
  name: "HomeView",
  setup() {
    console.log(this);

    const p = ref(null);
    const name = ref("mario");
    const age = ref(30);
    console.log(p, p.value);

    const handleClick = () => {
      console.log("You cliecked me", p, p.value);
      name = "luigi";
    };
    return { name, age, handleClick, p };
  },
};
</script>
