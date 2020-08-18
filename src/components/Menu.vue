<template>
  <div class="menu-container">
    <div class="logo-container">
      <router-link to="/">
        <img src="../assets/images/AngelaLogo.png" title="Angela's portfolio logo" />
      </router-link>
    </div>
    <div class="navs-container">
      <ul>
        <li>
          <router-link to="/">Home</router-link>
        </li>
        <li>
          <router-link to="/skills">Skills</router-link>
        </li>
        <li>
          <!-- <router-link to="/contact">Contact</router-link> -->
          <a href="mailto:future2931@gmail.com">Contact</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Menu'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.logo-container {
  padding: 3rem;
  text-align: center;
}

.navs-container {
  text-align: left;
  padding: 5rem 3rem;
}

li {
  padding-top: 1rem;
}

a {
  font-weight: bold;
  color: #333333;
  text-decoration: none;

  &:hover {
    color: #47c9e5;
  }

  &.router-link-exact-active {
    color: #47c9e5;
  }
}
</style>
