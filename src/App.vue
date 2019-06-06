<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
span {
  font-weight: bold;
}

#child-a, #child-b {
  width: 230px;
  padding: 5px;
  margin: 5px;
}

#child-a {
  background-color: sandybrown;
}

#child-b {
  background-color: mediumpurple;
}

#parent-a, #parent-b {
  width: 250px;
  padding: 5px;
  margin: 5px;
}

#parent-a {
  background-color: powderblue;
}

#parent-b {
  background-color: khaki;
}

#grandparent {
  background-color: darkseagreen;
  width: 270px;
  padding: 5px;
}
</style>
