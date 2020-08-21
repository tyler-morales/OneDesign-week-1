<template>
  <div class="latest-story">
    <div class="latest-story--block">
      <span class="latest-story--category">{{ latest.cat }}</span>
      <h2 class="latest-story--title">{{ latest.title }}</h2>
      <p class="latest-story--para">{{ latest.para }}</p>
      <span class="read-more--right">Read More</span>
    </div>
    <img class="latest-story--img" src="https://picsum.photos/150" alt="" />
  </div>
</template>

<script>
export default {
  props: {
    latest: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.latest-story {
  display: grid;
  grid-template-columns: 3fr 1fr;
  align-items: center;
  gap: 20px;

  @media (max-width: 600px) {
    grid-template-columns: 1fr;
  }

  &--block {
    // border-top: 2px solid #f6f6f6;
    padding: 20px 0;
  }

  &--category {
    text-transform: uppercase;
    color: #9e9e9e;
    font-size: 12px;
    letter-spacing: 0.1em;
  }

  &--title {
    margin: 10px 0;
  }

  &--para {
    color: #9e9e9e;
  }

  &--img {
    padding: 25px;
  }
}
</style>
