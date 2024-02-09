<script setup lang="ts">
import {ref} from "vue"

const pMsg = ref("イベント前ここをクリック");
const pBgColorEvent = ref("white");
const onPClickWithEvent = (bgColor: string, event: MouseEvent): void => {
  pBgColor.value = bgColor;
  pMsg.value = event.timeStamp.toString();
};
</script>

<template>
   <section>
      <p v-on:click="onPClickWithEvent('green', $event)" v-bind:style="{backgroundColor: pBgColorEvent}">
      ここをクリックすると背景色が変わります
      </p>
   </section>
</template>