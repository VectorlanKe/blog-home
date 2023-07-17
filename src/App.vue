<template>
  <main>
    <mindmap v-model="data"></mindmap>
  </main>
</template>
<script lang="ts" setup>
import mindmap from "vue3-mindmap";
import "vue3-mindmap/dist/style.css";

let data = [
  {
    name: "学习导图",
    children: [
      {
        name: "预备知识",
        children: [{ name: "HTML & CSS" }, { name: "JavaScript" }],
      },
      {
        name: "安装",
        collapse: true,
        children: [{ name: "折叠节点" }],
      },
      { name: "进阶", left: true },
    ],
  },
];
</script>