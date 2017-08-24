<template>
  <div>
    <sync-com :name.sync="parentName"></sync-com>
  </div>
</template>


<script>
  import syncCom from '~components/syncCom.vue'
  export default {
    components: {
      syncCom
    },
    data () {
      return {
        parentName: 'parentName..'
      }
    }
  }
</script>
<style>

</style>
