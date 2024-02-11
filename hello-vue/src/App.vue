<script setup lang="ts">
import {ref} from "vue"

const msg = ref("まだです");
const onEnterKey = (): void => {
  msg.value = "エンターキーが押下されました";
};
const onRightButtonClick = (): void => {
  msg.value = "ボタンが右クリックされました";
};
const onShiftClick = (): void => {
  msg.value = "シフトを押しながらクリックされました"
};

const inputNameBind = ref("しんちゃん");
const inputNameOn = ref('ななし');
const onInputName = (event: Event): void => {
  const element = event.target as HTMLInputElement;
  inputNameOn.value = element.value;
} 

</script>

<template>
  <section>
      <input type="text" v-bind:value="inputNameBind"><br>
  </section>
  <section>
      <input type="text" v-on:input="onInputName"><br>
      <button v-on:click.right="onRightButtonClick">右クリック</button><br>
      <p>{{ inputNameOn }}</p>
  </section>
</template>