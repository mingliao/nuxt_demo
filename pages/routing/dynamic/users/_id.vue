<template>
    <div>
      user detail page---》页面参数 id: {{paramId}}
      params 为context的一个属性。
      <a href="https://nuxtjs.org/guide/async-data" target="_blank">aysnc-data</a>
    </div>
</template>

<style>

</style>

<script>
    export default{
      validate ({ params }) {
        return /^\d+$/.test(params.id)
      },
      asyncData ({ params }, callback) {
        callback(null, { paramId: params.id })
      }
    }
</script>
