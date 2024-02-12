<script setup lang="ts">
import {ref} from "vue"

const inputTextarea = ref("テキストエリアへの入力文字");
const memberType = ref(1);
const memberTypeSelect = ref(1);
const onInputName = (event: Event): void => {
  const element = event.target as HTMLInputElement;
  inputNameOn.value = element.value;
} 

</script>

<template>
  <section>
      <input type="text" v-bind:value="inputNameBind"><br>
  </section>
  <br>
  <section>
      <input type="text" v-on:input="onInputName"><br>
      <p>{{ inputNameOn }}</p>
  </section>
</template>