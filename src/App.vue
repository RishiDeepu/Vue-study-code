<template>
  <h1 class="hed">VUE JS</h1>
  <img src="./assets/logo.png">
  <div class="a1">{{ greet }} {{ name }}</div>
  <div v-html="welcomeText"></div>
  <div v-html="click"></div>
  <div class="middle">
    <p v-bind:class="status">Vue is a framework and ecosystem that covers most of the common features needed in frontend
      development. But the web is extremely diverse - the things we build on the web may vary drastically in form and
      scale. With that in mind, Vue is designed to be flexible and incrementally adoptable. Depending on your use case,
      Vue can be used in different ways:

      Enhancing static HTML without a build step
      Embedding as Web Components on any page
      Single-Page Application (SPA)
      Fullstack / Server-Side Rendering (SSR)
      Jamstack / Static Site Generation (SSG)
      Targeting desktop, mobile, WebGL, and even the terminal
      If you find these concepts intimidating, don't worry! The tutorial and guide only require basic HTML and
      JavaScript knowledge, and you should be able to follow along without being an expert in any of these.

      If you are an experienced developer interested in how to best integrate Vue into your stack, or you are curious
      about what these terms mean, we discuss them in more details in</p>
    <br>
    <p v-bind:class="isRead ? 'yes' : 'no'">read above para first and understand what is vue</p>

    <h1 v-if="num === 0" class="a">number is Zero</h1>
    <h1 v-else-if="num > 0" class="b">number is Greater Than Zero {{ num }}</h1>
    <h1 v-else-if="num < 0" class="c">number is Less Than Zero {{ num }}</h1>
    <h1 v-else class="d"> not a number </h1>
  </div>
  <!-- object itteration-->
  <h3 v-for="i in sample" :key="i">{{ i }}</h3>
  <!-- Array itteration-->
  <h4 v-for="i in samp" :key="i">{{ i.name }} {{ i.age }} {{ i.team }}</h4>

  <h5>{{ add(1, 2) }}</h5>

</template>


<script>

export default {
  name: 'App',
  data() {
    return {
      name: "Rishi",
      greet: "Hey,How are you",
      welcomeText: "<b><i>Welcome to Vue <abbr title='JavaScript'>js</abbr></i></b>",
      click: "<a href='https://vuejs.org/guide/quick-start.html'target=”_blank”><i>Go To Doc</i></a>",
      status: "true",
      isRead: false,
      num: "dff",
      sample: {
        name: "test",
        age: 23,
        team: "india"
      },
      samp: [{
        name: "test",
        age: 23,
        team: "india"
      },
      {
        name: "test2",
        age: 23,
        team: "india"
      },
      ],
      mul: 1000
    }
  },
  methods: {
    add(a, b) {
      return (a + b) * this.mul;
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.hed {
  text-decoration: underline;
}

.middle {
  text-align: left;
}

.true {
  text-decoration: underline;
  color: green;
}

.false {
  font-style: italic;
  font-size: large;
  color: red;
}

.yes {
  font-size: x-small;
  color: green;
}

.no {
  font-size: large;
  color: red;
}

.a {
  color: green;
}

.b {
  color: blue;
}

.c {
  color: yellow;
}

.d {
  color: pink;
}
</style>
