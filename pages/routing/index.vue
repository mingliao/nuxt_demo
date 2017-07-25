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
          <template scope="scope">
            <span style="margin-left: 10px" class="level" :class="{warning: scope.row.level=='5'}">{{scope.row.desc}}</span>
          </template>
        </el-table-column>
      </el-table>



    </div>
</template>

<style lang="scss" >
  .level {

  }
  .level.warning {
    color: red;
  }
</style>

<script>
  export default{
    data () {
      return {
        routList: [{
          name: '基础路由',
          path: './routing/basic',
          desc: 'basic根目录',
          level: '1'
        }, {
          name: '基础路由',
          path: './routing/basic/demo',
          desc: 'basic/demo',
          level: '2'
        }, {
          name: '动态路由',
          path: './routing/dynamic',
          desc: '_表示参数',
          level: '3'
        }, {
          name: '嵌套路由',
          path: './routing/nested',
          desc: '',
          level: '4'
        }, {
          name: '动态嵌套路由',
          path: './routing/dynamic_nested',
          desc: '比较复杂，需要再看一下',
          level: '5'
        }]
      }
    }
  }
</script>
