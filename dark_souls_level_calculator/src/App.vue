<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <ClassSelection/>
    <LevelSection/>
    <AttributeSection/>
  </div>
</template>

<script>
import AttributeSection from './components/AttributesSection.vue'
import ClassSelection from './components/ClassSelection.vue'
import LevelSection from './components/LevelSection.vue'


export default {
  name: 'app',
  components: {
    AttributeSection,
    ClassSelection,
    LevelSection,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
