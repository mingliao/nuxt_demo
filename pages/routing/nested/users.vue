<template>
    <div>
      this is users .vue


      <el-input placeholder="请输入id" v-model="idInput">
        <template slot="prepend">goto</template>
      </el-input>
      ------------》下面是我的子页面      <nuxt-link :to="path">{{idInput}}</nuxt-link>



      <nuxt-child/>

    </div>
</template>

<style>

</style>

<script>
    export default{
      data () {
        return {
          idInput: '1'
        }
      },
      computed: {
        path: function () {
          return `./${this.idInput}`
        }
      }
    }
</script>
