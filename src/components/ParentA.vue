<template>
    <div id="parent-a">
        <h2>Parent A</h2>
        <pre>data {{ this.$data }}</pre>
        <button @click="reRender">Rerender Parent</button>
        <hr/>
        <child-a :score="score" @updateScore="updateScore"/>
        <child-b :score="score"/>
    </div>
</template>

<script>
import ChildA from './ChildA'
import ChildB from './ChildB'
export default {
  name: 'Parent A',
  data () {
    return {
      score: 100
    }
  },
  methods : {
        updateScore(newScore) {
            this.score = newScore;
        },
        reRender() {
            this.$forceUpdate()
        },
  },
  components: {
      ChildA, ChildB
  }
}
</script>