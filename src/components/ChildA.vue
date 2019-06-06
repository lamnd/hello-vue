<template>
    <div id="child-a">
      <h2>Child A</h2>
      <pre>data {{ this.$data }}</pre>
      <hr/>
      <button @click="changeScore">Change Score</button>
      <span>Score: {{ localScore }}</span>
    </div>
</template>

<script>
export default {
  name: 'Child A',
  props: ['score'],
  data: function() {
      return {
          localScore : this.score
      }
  },
  methods: {
        changeScore() {
            this.localScore += 100;
            this.$emit("updateScore", this.localScore);
        },

  }
}
</script>