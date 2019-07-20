<template>
  <v-content class="ma-0 pa-0">
    <div id="landing">
      <v-parallax
        id="parralax"
        src="https://scontent.fapa1-1.fna.fbcdn.net/v/t1.0-9/13438952_10157027950280335_1023770913506391617_n.jpg?_nc_cat=108&_nc_oc=AQkvq7F2nFEH9MyJhSqjfjwnOKgVfQ8Oh1jKpch29B9e3TtlojyAXuiG8JSIXAu_gUPvJxRDiNQWkO5bLNyxyVh2&_nc_ht=scontent.fapa1-1.fna&oh=8d8d8178e7f921e8e2511c7304f65439&oe=5DBF5CA4"
        style="height: 100%; opacity:0.7;"
      >
        <div>
          <h1 id="welcome">Welcome to my Portfolio</h1>
          <div id="my-div">
            <span v-bind:class="{active: isActive}" v-on:click="addActiveClass">A</span>
            Sean Hufnagel
          </div>
          <h2 id="uxui">User Experience / User Interface</h2>
          <h3 id="design">Designer / Developer</h3>
          <p id="learn">Learn about me!</p>
          <font-awesome-icon icon="coffee"></font-awesome-icon>
        </div>
      </v-parallax>
    </div>
    <div id="sec2">
      <h1>About</h1>
      <div></div>
      <div>
        <p>
          User-focused full stack web-developer that specializes in Javascript.
          Spent the last 5 years honing my technical skills to become a confident
          programmer, completing my Associates Degree in Computer Programming as
          well as earning my certificate at DU’s intensive web-development
          bootcamp program. I keep my head down and don’t stop until the job is
          and task is complete. I have 10 years experience in customer service
          so I am driven to provide an ideal User Experience in my products. I
          have advanced experience with web development languages including but
          not limited to HTML, CSS, Javascript, React & MySQL. Being a quick
          learner made it possible for me to grasp the context of programming
          language and move on to apply it. My optimistic spirit drives the whole
          team to excel and perform without hesitation, I strive to succeed with
          no alternative.
        </p>
      </div>
    </div>
    <div id="sec3">
      <v-flex id="skillsText">Skills</v-flex>
      <div id="skillBox">
        <v-parallax
          id="skillsBack"
          src="https://www.chainimage.com/images/apple-mac-os-x-lion-wallpapers-hd-desktop-wallpapers-pink-forest.jpg"
          style="height: 700px; opacity:0.8;"
        ></v-parallax>
      </div>
    </div>
    <div id="sec4">
      <h1>Portfolio</h1>
      <div id="projectBox"></div>
    </div>
    <div id="sec5">
      <h1>Resume</h1>
      <div id="resume">
        <v-img src="require('@/../../public/assets/photos/Sean Hufnagel - Resume.pdf')"></v-img>
      </div>
    </div>
    <div id="sec6">
      <h1>Contact</h1>
      <div id="resume"></div>
    </div>
  </v-content>
</template>


<script type="application/javascript" src="../../public/assets/js/animation.js"></script>
<script>
export default {
  data: () => ({
    drawer: null,
    isActive: true
  }),
  props: {
    source: String
  },
  methods: {
    addActiveClass: function() {
      return (this.isActive = !this.isActive);
    }
  },
  mounted() {
    if (window.innerWidth < 700) {
      // this.$router.push("HelloWorld");
      console.log("Mobile");
    }
  }
};
</script>

<style scoped>
#sec2,
#sec3,
#sec4,
#sec5,
#sec6 {
  width: 110%;
  position: relative;
  right: 3%;
  height: 700px;
}
#sec2 {
  background-color: rgba(211, 211, 211, 0.411) !important;
}
#sec3 {
  /* background-color: rgba(255, 186, 58, 0.692); */
}
#sec6 {
  background-color: rgba(11, 11, 88, 0.479);
}
h1,
p {
  text-align: center;
}
#uxui {
  text-align: center;
  color: black;
}
#design {
  text-align: center;
  color: black;
}
#learn {
  color: black;
  text-align: center;
}
#skillsBack {
  margin-top: -90px;
  z-index: 0;
}
#skillsText {
  z-index: 9999;
  color: black;
  opacity: 0.9;
  text-align: center;
  font-size: 36px;
}
#welcome {
  text-align: center;
  position: relative;
  font-family: sans-serif;
  text-transform: uppercase;
  font-size: 2em;
  letter-spacing: 4px;
  overflow: hidden;
  background: linear-gradient(90deg, #000, #fff, #000);
  background-repeat: no-repeat;
  background-size: 80%;
  animation: animate 3s linear infinite;
  -webkit-background-clip: text;
  -webkit-text-fill-color: rgba(255, 255, 255, 0);
}
@keyframes animate {
  0% {
    background-position: -500%;
  }
  100% {
    background-position: 500%;
  }
}
#parralax {
  width: 110%;
  right: 3.5%;
}
#landing {
  height: 800px;
}
</style>