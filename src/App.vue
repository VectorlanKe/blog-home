<template>
  <main>
    <div  class="mindmap">
      <mindmap v-model="data" branch="1"></mindmap>
    </div>
  </main>
</template>
<script lang="ts" setup>
import mindmap from "vue3-mindmap";
import "vue3-mindmap/dist/style.css";
import mindMapJson from "@/assets/mindmap.json"

let data =mindMapJson;
</script>
<style>
.mindmap{
  float: left;
  margin-top: 20vh;
  width: 100vw;
  height: 60vh;
  font-size:smaller
}
</style>