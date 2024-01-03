<template>
  <div>{{ msg }}</div>
  <pre>{{ msg2 }}</pre>
</template>

<script>
export default {
  name: 'LessonFirst',
  props: {
    msg: String
  },
  data: function() {
    return {
      msg2: 'おおきに'
    };
  }
}
</script>

<style scoped>

</style>