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

  @media (max-width: 600px) {
    display: grid;
    gap: 5px;
  }

  &--home {
    font-weight: 500;
    font-size: 28px;
  }

  &__links {
    width: max-width;
    font-weight: 300;

    & > * {
      padding: 0 10px;

      @media (max-width: 600px) {
        padding: 0;
        padding-right: 10px;
      }
    }
  }

  &__account {
    & > * {
      padding: 0 10px;

      @media (max-width: 600px) {
        padding-left: 0;
      }

      &:last-child {
        padding-right: 0;
      }
    }
  }
}

a {
  text-decoration: none;
  color: inherit;
}
</style>
