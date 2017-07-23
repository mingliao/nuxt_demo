<template>
    <div>
      <el-table
        :data="routList"
        style="width: 980px;margin-top: 20px;">
        <el-table-column
          prop="name"
          label="名称"
          align="center"
        >
        </el-table-column>
        <el-table-column
          prop="path"
          label="地址"
          align="center"
        >
          <template scope="scope">
            <el-icon name="time"></el-icon>
            <span style="margin-left: 10px"><nuxt-link v-bind:to="scope.row.path">{{scope.row.path}}</nuxt-link></span>
          </template>
        </el-table-column>
        <el-table-column
          prop="desc"
          align="center"
          label="简要说明">
        </el-table-column>
      </el-table>



    </div>
</template>

<style>

</style>

<script>
  export default{
    data () {
      return {
        routList: [{
          name: '基础路由',
          path: './routing/basic',
          desc: 'basic根目录'
        }, {
          name: '基础路由',
          path: './routing/basic/demo',
          desc: 'basic/demo'
        }, {
          name: '动态路由',
          path: './routing/dynamic',
          desc: '_表示参数'
        }, {
          name: '嵌套路由',
          path: './routing/nested',
          desc: ''
        }]
      }
    }
  }
</script>
