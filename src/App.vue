<template>
  <div id="app">
    <section>
      <div class="heading">
        We make creative media that <span>adds value</span>
      </div>

      <div class="card-container">
        <div class="col" v-for="item in items" :key="item.id">
          <Card :cardItem="item" />
        </div>
      </div>
      <div class="center">
        <span role="button" class="btn">get started</span>
      </div>
    </section>
  </div>
</template>

<script>
import Card from "./components/Card.vue";

export default {
  name: "App",
  components: {
    Card,
  },
  data() {
    return {
      items: [
        {
          id: 1,
          img: require(`@/assets/1.png`),
          title: "Photography",
          list: ["Drone Photography", "Interiors", "Exteriors / Architectural"],
          desc: "Every photograph we produce finds the beauty in your property while serving as a profitable asset.",
        },
        {
          id: 2,
          img: require(`@/assets/2.png`),
          title: "Virtual Staging",
          list: [],
          desc: "Our staging will help you sell the potential of your space.We can work off of our own photography or photos you provide.",
        },
        {
          id: 3,
          img: require(`@/assets/image9.png`),
          title: "Renderings",
          list: ["Interiors", "Exteriors"],
          desc: "Renderings are the gold standard in pre-construction marketing.",
        },
        {
          id: 4,
          img: require(`@/assets/image10.png`),
          title: "Interactive Tours",
          list: ["Matterport", "Video Walkthroughs"],
          desc: "Give your audience the ability to explore your property without requiring in-person travel.",
        },
        {
          id: 5,
          img: require(`@/assets/image11.png`),
          title: "Floor Plans",
          list: ["On-site Measure", "2D Floor Plans", "3D Floor Plans"],
          desc: "We produce laser-precise floor plans faster than any other service.",
        },
        {
          id: 6,
          img: require(`@/assets/image12.png`),
          title: "Video",
          list: [
            "Drone Cinematography",
            "Interiors",
            "Exteriors / Architectural",
          ],
          desc: "Video content has higher engagement and will help your property stand out online.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
body {
  background: #e5e5e5;
  box-sizing: border-box;
  line-height: 1.5;
}
#app {
  font-family: "Poppins", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  max-width: 1400px;
  width: 100%;
  margin: auto;
  padding: 1rem;
  section {
    margin-top: 3rem;
    .heading {
      color: #1b264f;
      font-weight: 700;
      font-size: 56px;
      line-height: 1.5;
      text-align: center;
      max-width: 750px;
      width: 100%;
      margin: auto;
      margin-bottom: 3rem;
      span {
        color: #506bca;
      }
      @media (max-width: 768px) {
        font-size: 2.5rem;
      }
      @media (max-width: 500px) {
        font-size: 1.75rem;
      }
    }
    .card-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      .col {
        width: 32.5%;
        margin-bottom: 1rem;
        height: 100%;
        @media (max-width: 1200px) {
          width: 49%;
        }
        @media (max-width: 768px) {
          width: 100%;
        }
      }
    }
  }
}
.center {
  text-align: center;
  margin: 2rem auto;
}
.btn {
  padding: 20px 58px;
  gap: 10px;
  width: 315px;
  height: 60px;
  background: #1b264f;
  border-radius: 12px;
  text-align: center;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  font-weight: 700;
  font-size: 17px;
  line-height: 60px;
  color: #ffffff;
  cursor: pointer;
}
</style>