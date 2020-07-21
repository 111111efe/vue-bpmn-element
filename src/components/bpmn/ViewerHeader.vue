<template>
  <div>
    <el-button-group>
      <el-button type="primary" size="mini" title="保存并发布" icon="el-icon-s-order" @click="deploy">保存并发布</el-button>
      <el-button type="primary" size="mini" title="保存并发布" icon="el-icon-s-order" @click="start">启动实例</el-button>
    </el-button-group>
  </div>
</template>

<script>
  import './vue-bmpn.css'
  export default {
    name: "ViewerHeader",
    data(){
      return {
        xmlVisible:false
      }
    },
    props:{
      processData:{
        type:Object
      }
    },
    components:{
    },
    methods:{
      deploy(){
        this.$emit('handleDeploy')
      },
      start(){
        this.$emit('handleStart')
      }
    }
  }
</script>

<style scoped>
  .icon-header{
    font-size: 14px;
  }

</style>
