<template>
  <div class="home">
    <div class="home__hero">
      <div>
        <span class="home__hero--category">Stories</span>
        <h1 class="home__hero--title">The Canyons</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi est
          pariatur facere suscipit dolorem fugiat, porro corporis possimus
          molestiae at.
        </p>
        <div class="read-more">
          <span>Read More</span>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="36"
            height="36"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="1"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="feather feather-arrow-down-circle"
          >
            <circle cx="12" cy="12" r="10"></circle>
            <polyline points="8 12 12 16 16 12"></polyline>
            <line x1="12" y1="8" x2="12" y2="16"></line>
          </svg>
        </div>
      </div>
    </div>

    <div class="grid">
      <div class="grid__featured">
        <h2 class="section--title">Featured Stories</h2>
        <div class="grid__featured__container">
          <Featured
            v-for="(feature, index) in features"
            :key="index"
            :feature="feature"
          />
        </div>
      </div>
      <div class="grid__latest">
        <h2 class="section--title">Latest Stories</h2>
        <div class="grid__latest__container">
          <LatestCard
            v-for="(latest, index) in latests"
            :key="index"
            :latest="latest"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Featured from '@/components/Featured'
import LatestCard from '@/components/LatestCard'
export default {
  components: {
    Featured,
    LatestCard
  },
  data: function() {
    return {
      features: [
        {
          title: 'Explore the Mountains',
          description:
            'Democracy never lasts long. It soon wastes, exhausts and murders itself. There was never a democracy that did not commit suicide."',
          img: 'https://picsum.photos/800'
        }
      ],
      latests: [
        {
          cat: 'Stories',
          title: 'Rising Above the Clouds',
          para:
            'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sed, consectetur!'
        },
        {
          cat: 'Stories',
          title: 'Rising Above the Clouds',
          para:
            'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sed, consectetur!'
        },
        {
          cat: 'Stories',
          title: 'Rising Above the Clouds',
          para:
            'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sed, consectetur!'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.home {
  margin-top: 40px;

  h2 {
    font-weight: 500;
  }

  &__hero {
    background-image: url('../assets/images/iceland.jpg');
    text-align: center;
    color: white;
    min-height: 70vh;
    display: grid;
    place-items: center;
    background-size: cover;

    &--category {
      text-transform: uppercase;
      letter-spacing: 0.141em;
      margin: 0;
    }
    &--title {
      font-size: 72px;
      margin: 10px;

      @media (max-width: 600px) {
        font-size: 36px;
      }
    }

    p {
      font-size: 18px;
      width: 50vw;
      margin: 0 auto;
      line-height: 2;
      font-weight: 300;

      @media (max-width: 600px) {
        font-size: 14px;
        line-height: 1.6;
        width: 80%;
      }
    }

    .read-more {
      display: flex;
      flex-direction: column;
      margin-top: 100px;
      justify-content: center;
      gap: 10px;

      @media (max-width: 600px) {
        margin-top: 20px;
      }

      svg {
        margin: 0 auto;
      }
    }
  }

  .grid {
    display: grid;
    gap: 50px;
    grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
    margin-top: 10px;

    @media (max-width: 600px) {
      gap: 20px;
    }

    .section--title {
      margin-bottom: 30px;
    }

    & > * {
      max-width: 90vw;
    }

    &__latest {
      &__container {
        & > * {
          border-top: 2px solid #f6f6f6;
          &:last-child {
            border-bottom: 2px solid #f6f6f6;
          }
        }
      }
    }
  }
}
</style>
