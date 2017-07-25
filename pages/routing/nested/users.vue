<template>
    <div>
      <h2 class="title">nested route </h2>
      <el-input placeholder="请输入id" v-model="idInput">
        <template slot="prepend">goto the next page</template>
      </el-input>
      下面是我的子页面      <nuxt-link :to="path">{{idInput}}</nuxt-link>

      <div style="border:2px solid #000">
        <nuxt-child/>
      </div>


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
          return `/routing/nested/users/${this.idInput}`
        }
      }
    }
</script>
