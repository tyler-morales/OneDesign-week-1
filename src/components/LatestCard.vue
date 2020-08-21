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
  max-width: 90vw;

  &--block {
    padding: 20px 0;
  }

  &--category {
    text-transform: uppercase;
    color: #9e9e9e;
    font-size: 12px;
    letter-spacing: 0.1em;

    @media (max-width: 400px) {
      font-size: 10px;
    }
  }

  &--title {
    margin: 10px 0;
    @media (max-width: 400px) {
      font-size: 14px;
      margin: 0;
    }
  }

  &--para {
    color: #9e9e9e;
    @media (max-width: 400px) {
      font-size: 12px;
    }
  }

  &--img {
    padding: 25px;

    @media (max-width: 600px) {
      padding: 0;
    }
    @media (max-width: 400px) {
      width: 100px;
    }
  }

  .read-more--right {
    @media (max-width: 400px) {
      font-size: 12px;
    }
  }
}
</style>
