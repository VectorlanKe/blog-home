<template>
  <main>
    <div class="mindmap">
      <mindmap v-model="data" branch="2" zoom="true"></mindmap>
    </div>
    <div class="entrance-root">
      <div class="entrance" @click="blankBlog()">进入博客</div>
    </div>
    <footer>
      <div>
        <img src="../public/备案图标.png" />
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
import "@/assets/stars.css";
import mindMapJson from "@/assets/mindmap.json";
let data = mindMapJson;
function blankBlog(): void {
  window.open("https://blog.vectorluo.top",'_self');
}
</script>
<style lang="less">
main{
  color: #fff;
}
.mindmap {
  position: fixed;
  float: left;
  width: 100%;
  height: 80vh;
  font-size: 0.8em;
  overflow:visible;
  cursor:grab;
}
.mindmap:active{
  cursor:grabbing;
}

.mindmap svg {
  background: none;
  tspan{
    fill: #fff;
  }
  .Mindmap_root_fgvb6>.Mindmap_content_fgvb6>.Mindmap_text_fgvb6 {
    rect{
      stroke: #dcdcdc;
    }
    text>tspan{
      fill: #000;
    }
  }
}
.entrance-root {
  position: fixed;
  width: 100%;
  bottom: 120px;
}
.entrance {
  position: relative;
  margin: 0 auto;
  width: 150px;
  height: 40px;
  line-height: 40px;
  text-align: center;
  font-size: 1em;
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
  bottom: 25px;
  div {
    width: 474px;
    margin: 0 auto;
    img {
      float: left;
      margin: 1px 4px;
    }
  }
  a,
  a:link,
  a:visited,
  a:active {
    color: #fff;
    text-decoration: none;
  }
}
</style>