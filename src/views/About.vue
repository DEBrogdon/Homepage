<template>
  <div class="about">
    <div class="container-fluid">
      <div class="row no-gutter">
        <div class="col">
          <h1 class="font-medium title-text">About</h1>
        </div>
      </div>
      <div class="row no-gutter">
        <div class="col">
          <div class="profile-text-container">
            <p>Hello! I'm a Software Developer located in Norman, OK.</p>
            <p>I have exerience in leading teams, front-end, back-end, and UI/UX work.</p>
            <p>Browse some of my <router-link to="/projects" class="link-text">work</router-link>, my <router-link to="/templates" class="link-text">templates</router-link>, or <router-link to="/contact" class="link-text">get in touch</router-link></p>
            <p>You can also find me at <a class="link-text" :href="github">Github</a> or <a class="link-text" :href="linkedin">Linkedin</a></p>
          </div>
        </div>
        <div class="col">
          <div class="profile-skills-container">
            <div class="row no-gutter">
              <div class="col">
                <h5 style="border-top: 1px solid black;">Languages</h5>
                <li v-for="(language, index) in languages" :key="`language-${index}`">
                  <p class="skills-text">{{language}}</p>
                </li>
              </div>
              <div class="col">
                <h5 style="border-top: 1px solid black">Frameworks</h5>
                <li v-for="(framework, index) in frameworks" :key="`framework-${index}`">
                  <p class="skills-text">{{framework}}</p>
                </li>
              </div>
              <div class="col">
                <h5 style="border-top: 1px solid black">Tools</h5>
                <li v-for="(tool, index) in tools" :key="`tool-${index}`">
                  <p class="skills-text">{{tool}}</p>
                </li>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "about",
    data() {
      return {
        linkedin: "https://www.linkedin.com/in/donbrogdon/",
        github: "https://github.com/ApproximatelyInfinity",
        codepen: "https://www.codepen.com/",
        dribble: "https://www.dribble.com/",
        languages: ["C/C++", "PHP", "Javascript", "HTML/CSS", "MySQL"],
        frameworks: ["Vue.js", "jQuery", "SASS", "Bootstrap", "WordPress"],
        tools: ["Photoshop", "Illustrator", "Visual Studio Code"],
      }
    }
  }
</script>

<style scoped lang="scss">
@import './src/style/globals.scss';
@import './src/style/fonts.scss';

li {
  list-style-type: none;
}

.title-text {
  margin-left: 10px;
  font-weight: 200;
  border-bottom: 1px solid black;
  margin-right: 10px;
}

.profile-text-container {
  margin-left: 10%;
  margin-top: 20%;
}

.link-text {
 color: map-get($colors, secondary);
 font-weight: bold;
}
.link-text:hover {
   color: map-get($colors, primary);
}

.profile-skills-container {
  margin-right: 10%;
  margin-top: 20%;
}
.skills-text {
  margin-top: -6px;
  margin-bottom: 6px;
}
</style>