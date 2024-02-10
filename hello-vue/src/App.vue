<script setup lang="ts">
import {ref} from "vue"

const msg = ref("まだです");
const onEntryKey = (): void => {
  msg.value = "エンターキーが押下されました";
};
const onRightButtonClick = (): void => {
  msg.value = "ボタンが右クリックされました";
};
const onShiftClick = (): void => {
  msg.value = "シフトを押しながらクリックされました"
};
</script>

<template>
   <section>
      <form action="#" v-on:submit="onFormSubmit">
      <input type="text" required>
      <button type="submit">送信</button>
    </form>
    <p>{{ msg }}</p>
   </section>
</template>