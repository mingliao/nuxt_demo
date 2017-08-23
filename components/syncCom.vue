<template>
    <div>
        ---------->{{name}}
      <button @click="test">test</button>
    </div>
</template>
<script>
    export default {
      props: ['name'],
      methods: {
        test () {
          this.$emit('update:name', 'new CHild name')
        }
      }
    }
</script>
<style>

</style>
