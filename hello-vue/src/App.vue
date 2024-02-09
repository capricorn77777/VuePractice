<script setup lang="ts">
import {ref} from "vue"

const pBgColor = ref("white");
</script>

<template>
   <section>
      <img src="./assets/logo.svg" alt="Vueのロゴ" width="200" v-on:mousemove="onImgMousemove">
      <p>ポインタの位置： x={{ mousePointerX }}; y={{ mousePointerY }}</p>
   </section>
</template>