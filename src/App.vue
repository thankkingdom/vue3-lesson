<template>
  <!--<img alt="Vue logo" src="./assets/logo.png">-->
  <LessonFirst msg="まいど"/>
  <WonderingMonster v-for="item in monsters"
    v-bind:key="item.id" v-bind="item"
    v-on:attack="handleAttack"
    ref="monster">
  </WonderingMonster>
</template>

<script>
import LessonFirst from './components/LessonFirst.vue'
import WonderingMonster from './components/WonderingMonster.vue'

export default {
  name: 'App',
  components: {
    LessonFirst,
    WonderingMonster,
  },
  data: function() {
    return {
      monsters: [
        { id: 1, name: 'スライム', hp: 100, image: '/image/slime.jpg' },
        { id: 2, name: 'ゴブリン', hp: 200, image: '/image/DnD_Goblin.png' },
        { id: 3, name: 'ドラゴン', hp: 500, image: '/image/dragon.jpg' }
      ]
    }
  },
  methods: {
    handleAttack: function(id) {
      var item = this.monsters.find(function(el) {
        return el.id === id
      });
      if (item !== undefined && item.hp > 0) {
        item.hp -= 10;
      } else {
        alert('Help me!');
      }
    },
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
