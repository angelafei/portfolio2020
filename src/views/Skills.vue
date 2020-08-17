<template>
  <div class="skills-container">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <SkillItem v-bind:level="2" />
  </div>
</template>

<script>
// @ is an alias to /src
import SkillItem from '@/components/SkillItem.vue'

export default {
  name: 'Skills',
  components: {
    SkillItem
  }
}
</script>

<style scoped lang="scss">
.skills-container {
  padding: 2rem;
}
</style>
