<template>
  <nav class="nav">
    <div class="nav--home">
      <router-link to="/">Nomadic</router-link>
    </div>
    <div class="nav__links">
      <router-link to="/stories">Stories</router-link>—
      <router-link to="/photos">Photos</router-link>—
      <router-link to="/gear">Gear</router-link>
    </div>
    <div class="nav__account">
      <span>Sign Up</span>|
      <span>Login</span>
    </div>
    <!-- <router-view /> -->
  </nav>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.nav {
  margin-top: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;

  &--home {
    font-weight: 500;
    font-size: 24px;
  }

  &__links {
    width: max-width;
    font-weight: 300;

    & > * {
      padding: 0 10px;
    }
  }

  &__account {
    & > * {
      padding: 0 10px;
    }
  }
}

a {
  text-decoration: none;
  color: inherit;
}
</style>
