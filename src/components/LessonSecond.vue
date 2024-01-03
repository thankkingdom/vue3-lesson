<template>
  <WonderingMonster v-for="item in monsters"
    v-bind:key="item.id" v-bind:name="item.name" v-bind:hp="item.hp">
  </WonderingMonster>
</template>

<script>
export default {
  name: 'LessonSecond',
  props: {
    monsters: [
      { id: 1, name: 'スライム', hp: 100 },
      { id: 2, name: 'ゴブリン', hp: 200 },
      { id: 3, name: 'ドラゴン', hp: 500 }
    ]
  }
}
</script>