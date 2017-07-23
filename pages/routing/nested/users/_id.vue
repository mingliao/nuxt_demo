<template>
    <div>
      user detail--{{paramId}}
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
