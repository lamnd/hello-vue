<template>
    <div id="child-b">
      <h2>Child B</h2>
      <pre>data {{ this.$data }}</pre>
      <hr/>
      <span> Show Score: {{ score }}</span>
    </div>
</template>

<script>
export default {
  name: 'Child A',
  props: ['score'],
}
</script>