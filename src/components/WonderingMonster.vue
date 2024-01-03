<template>
  <div>
    <hr>
    <div>Name: {{ name }}, HP: {{ hp }}</div>
    <img :src="image" height="100px">
    <!--<img src="../assets/logo.png">-->
    <button v-on:click="doAttack">攻撃する</button>
  </div>
</template>

<script>
export default {
  name: 'WonderingMonster',
  props: {
    id: Number,
    name: String,
    hp: Number,
    image: String,
  },
  methods: {
    doAttack: function() {
      this.$emit('attack', this.id);
    },
  },
}
</script>