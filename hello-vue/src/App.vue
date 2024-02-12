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
  <textarea v-model="inputTextarea"></textarea>
  <br>
  <section>
      <label><input type="radio" name="memberType" value="1" v-model="memberType">通常会員</label>
      <label><input type="radio" name="memberType" value="2" v-model="memberType">特別会員</label>
      <label><input type="radio" name="memberType" value="3" v-model="memberType">優良会員</label>
      <br>
      <p>選択されたラヂオボタン: {{ memberType }}</p>
  </section>
  <br>
  <section>
      <select v-model="memberTypeSelect">
        <option value="1">通常会員</option>
        <option value="2">通常会員</option>
        <option value="3">通常会員</option>
      </select>
  </section>
</template>