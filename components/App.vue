<template>
  <div class="start_screen">
    <h1>{{ title }}</h1>
    <button v-on:click="startGame">{{ buttonText }}</button>
    <p>{{ firstScript }}</p>
  </div>
</template>

<style lang="stylus" scoped>
  .show_button{
    display: none;
  }
</style>

<script>
export default {
  data() {
    return {
      title: `An Adventure to Another World`,
      buttonText: `Start Game`,
      showButton: ``,
      firstScript: ``,
      isGame: false
    }
  },
  methods: {
    startGame() {
      this.isGame = !this.isGame;
      this.buttonText = `Next`;
      this.title = this.isGame ? `How to Play` : `An Adventure to Another World`;
    }
  }
}
</script>>
