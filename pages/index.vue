<template>
  <section class="container">

    <div>
      <logo/>
      <h1 class="title">
        NUXT
      </h1>
      <h2 class="subtitle">
        Universal Vue.js Application
      </h2>
      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green">Documentation</a>
        <a href="https://github.com/nuxt/nuxt.js" target="_blank" class="button--grey">GitHub</a>
        <a href="http://element.eleme.io/#/zh-CN" target="_blank" class="button--grey">element-ui</a>
      </div>



      <el-table
        :data="tableData"
        style="width: 980px;margin-top: 20px;">
        <el-table-column
          prop="date"
          label="主题"
          align="center"
        >
        </el-table-column>
        <el-table-column
          prop="name"
          label="地址"
          align="center"
        >
          <template scope="scope">
            <el-icon name="time"></el-icon>
            <span style="margin-left: 10px"><nuxt-link v-bind:to="scope.row">{{scope.row.name}}</nuxt-link></span>
          </template>
        </el-table-column>
        <el-table-column
          prop="address"
          align="center"
          label="简要说明">
        </el-table-column>
      </el-table>

    </div>

  </section>
</template>

<script>
import Logo from '~components/Logo.vue'

export default {
  components: {
    Logo
  },
  data () {
    return {
      tableData: [{
        date: '路由',
        name: 'routing',
        address: '路由一些用法'
      }, {
        date: '2016-05-04',
        name: '王小虎1',
        address: '上海市普陀区金沙江路 1517 弄'
      }, {
        date: '2016-05-01',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1519 弄'
      }, {
        date: '2016-05-03',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1516 弄'
      }]
    }
  }
}
</script>

<style>
.container
{
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.title
{
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.subtitle
{
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
.links
{
  padding-top: 15px;
}
</style>
