<template>
  <div>
    <!-- <h3 class="thin" :class=" isItalic ? 'italic': '' ">MyStyle 组件</h3> -->
    <!-- <h3 class="thin" :class=" [isItalic ? 'italic': '',isDelete?'delete':''] ">MyStyle 组件</h3>
    <button @click="isItalic = !isItalic">Toggle Italic</button>
    <button @click="isDelete = !isDelete">Toggle Delete</button> -->
    <h3 class="thin" :class="classObj">MyStyle 组件</h3>
    <button @click="classObj.italic = !classObj.italic">Toggle Italic</button>
    <button @click="classObj.delete = !classObj.delete">Toggle Delete</button>
    <hr>
    <div :style="{ color: active,fontSize:fsize+'px',backgroundColor:bgcolor }">黑马程序员</div>
    <button @click="fsize+=1">字号 +1</button>
    <button @click="fsize-=1">字号 -1</button>
  </div>
</template>

<script>
export default {
  name:'MyStyle',
  data() {
    return {
      isItalic:false,
      isDelete:false,
      classObj :{
         italic:false,
         delete:false,
      },
      active:'red',
      fsize:30,
      bgcolor:'pink'
    }
  },
}
</script>

<style lang="less">
  .thin{
    font-weight: 7100;
  }
  .italic {
    font-style: italic;
  }
.delete {
  text-decoration: line-through;
}
</style>