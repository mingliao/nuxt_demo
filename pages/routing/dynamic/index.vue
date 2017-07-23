<template>
    <div>
      this is dynamic route    goto the input val detail

      <el-input placeholder="请输入id" v-model="idInput">
        <template slot="prepend">goto</template>
      </el-input>
      <nuxt-link :to="path">goto -->{{idInput}} user detail</nuxt-link>

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
          return `./dynamic/users/${this.idInput}`
        }
      }
    }
</script>
