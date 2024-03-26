<template>
  <q-page class="fundo flex flex-center">
    <div class="card bg-dark"
         style="border-radius: 100px;
                width: 80vw; height: 70vh;
                box-shadow: 1px 1px 10px 0.5px white"
         :style="boo ? 'animation-name: mais_info' : ''"
         ref="card">
      <q-btn class="bg-white" @click="teste">teste</q-btn>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from 'vue';

defineOptions({
  name: 'IndexPage',
});

const card = ref('');
const boo = ref(false);

const teste = () => {
  // card.value.style.animationName = 'mais_info';
  boo.value = !boo.value;
};
</script>
<style>
  .fundo {
    background-image:
      linear-gradient(rgba(18, 18, 18, 0.60),rgba(18, 18, 18, 0.95)),
      url("src/assets/5539148.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    width: 100%;
    height: 100%;
  }
  .card {
    animation-duration: 2s;
    animation-timing-function: ease-in;
    animation-fill-mode: forwards;
  }
  @keyframes mais_info {
    from {width: 80vw; height: 70vh}
    to{width: 100vw; height: 100vh; border-radius: 0px}
  }
</style>
