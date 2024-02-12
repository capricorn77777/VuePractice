<script setup lang="ts">
import {ref} from "vue"

const inputTextarea = ref("テキストエリアへの入力文字");
const memberType = ref(1);
const memberTypeSelect = ref(1);
const isAgreed = ref(false);
const isAgreed01 = ref(0);
const selectedOS = ref([]);
const selectedOSSelect = ref([]);

</script>

<template>
  <Ap
  <section>
      <input type="text" v-bind:value="inputNameBind"><br>
  </section>
  <br>
  <section>
      <input type="text" v-on:input="onInputName"><br>
      <p>{{ inputNameOn }}</p>
  </section>
</template>