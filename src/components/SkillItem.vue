<template>
  <div class="skill-item-container">
    <img src="../assets/images/photoshop.png" />
    <span>Photoshop</span>
    {{level}}
  </div>
</template>

<script>
export default {
  name: 'SkillItem',
  props: {
    level: Number
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.skill-item-container {
  position: relative;
  padding-left: 10px;
  box-shadow: 1px 1px 2px 1px rgba(0, 0, 0, 0.1);
  display: flex;
  align-items: center;
  border-radius: .2rem;
  overflow: hidden;

  &:before {
    width: 6px;
    content: "";
    background: red;
    position:absolute;
    top:0;
    bottom:0;
    left:0;
  }
}
</style>
