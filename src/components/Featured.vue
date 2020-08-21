<template>
  <div class="feature--img" :style="imageStyleObject">
    <h3>{{ feature.title }}</h3>
    <p>{{ feature.description }}</p>
  </div>
</template>

<script>
export default {
  props: {
    feature: {
      type: Object,
      required: true
    }
  },
  computed: {
    imageStyleObject() {
      return {
        backgroundImage: `
          linear-gradient(to bottom,rgba(245, 246, 252, 0) 45%,rgb(0, 0, 0) 100%), 
          url(${this.feature.img})
        `,
        backgrountRepeat: 'no-repeat',
        backgroundSize: 'cover',
        backgroundPosition: 'center'
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.feature--img {
  margin: 40px 0;
  min-height: 50vh;
  background-size: cover;
  color: white;
  padding: 40px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  max-width: 90vw;

  &:last-child {
    margin-bottom: 0;
  }

  h3 {
    font-size: 22px;
    margin: 0;
  }
}
</style>
