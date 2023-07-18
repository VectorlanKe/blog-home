<template>
  <main>
    <div class="mindmap">
      <mindmap v-model="data" branch="1"></mindmap>
    </div>
    <div class="entrance-root">
      <div class="entrance" @click="blankBlog()">进入博客</div>
    </div>
    <footer>
      <div>
        <img src="../public/备案图标.png"/>
        <a
          href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=51012202001211"
          target="_blank"
          >川公网安备 51012202001211号</a
        >&nbsp;&nbsp;|&nbsp;&nbsp;
        <a href="https://beian.miit.gov.cn/" target="_blank"
          >蜀ICP备2022010806号-1</a
        >
      </div>
    </footer>
  </main>
</template>
<script lang="ts" setup>
import mindmap from "vue3-mindmap";
import "vue3-mindmap/dist/style.css";
import mindMapJson from "@/assets/mindmap.json";
let data = mindMapJson;
function blankBlog(): void {
  window.open("https://blog.vectorluo.top");
}
</script>
<style lang="less">
.mindmap {
  float: left;
  margin-top: 20vh;
  width: 100vw;
  font-size: 0.8em;
}

.mindmap svg {
  background: none;
  .Mindmap_text_fgvb6 > rect {
    stroke: beige;
  }
}
.entrance-root {
  position: fixed;
  width: 100%;
  bottom: 300px;
}
.entrance {
  position: relative;
  margin: 0 auto;
  width: 150px;
  height: 40px;
  line-height: 40px;
  text-align: center;
  font-size: 1em;
  color: #5c5c5c;
  border: 1px solid #888888;
  border-radius: 0.5em;
  cursor: pointer;
}
.entrance:hover {
  color: white;
  background: #1897ff;
  border: 0;
}
footer {
  position: fixed;
  width: 100%;
  bottom: 10px;
  div {
    width: 474px;
    margin: 0 auto;
    img{
      float: left;
      margin: 1px 4px;
    }
  }
  a,a:link,a:visited,a:active{
    color: #424242;
    text-decoration: none;
  }
}
</style>