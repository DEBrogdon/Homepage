<template>
  <div class="home">
    <div class="container-fluid">
      <div class="row no-gutter">
        <div class="col">
          <div class="home-text-container">
            <div class="row no-gutter">
              <div class="col-sm">
                <p class="font-heavy name">Don Brogdon,</p>
              </div>
            </div>
            <div class="row no-gutter">
              <div class="col-sm">
                <p class="font-medium title">Developer<span class="animated-flash animated flash">_</span></p>
              </div>
            </div>
            <div class="row no-gutter">
              <div class="col-sm">
                <p class="font-light detail">I produce elegant, performant, and accessible digitial experiences.</p>
              </div>
            </div>
            <div class="row no-gutter">
              <div class="col-sm">
                <router-link to="/projects">
                  <button class="btn-outline-dark btn-desktop btn-toggle-background" type="button">Explore Work
                    <span class="background-btn-left-home"></span>
                    <span class="background-btn-bottom-home"></span>
                  </button>
                </router-link>
                <span style="margin-right: 32px;"></span>
                <router-link to="/resume">
                  <button class="btn-outline-dark btn-desktop btn-toggle-background" type="button">View Profile
                    <span class="background-btn-left-home2"></span>
                    <span class="background-btn-bottom-home2"></span>
                  </button>
                </router-link>
              </div>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="home-img-container">
            <HelloWorld/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
@import './src/style/globals.scss';
@import './src/style/buttons.scss';
@import './src/style/fonts.scss';
.animated-flash {
  animation-iteration-count: infinite;
}
.name {
  font-size: 60px;
}
.title {
  font-size: 50px;
  margin-top: -32px;
}
.detail {
  font-size: 24px;
  margin-top: -16px;
  margin-left: 5px;
}
.home-text-container {
	margin-top: 25%;
	margin-left: 10%;
}
.home-img-container {
	margin-top: 10%;
  margin-left: 20%;
}
.background-btn-left-home {
    position: absolute;
    margin-top: -31px;
    margin-left: -60px;
    display: none; 
}
.background-btn-bottom-home {
    position: absolute;
    margin-top: 9px;
    margin-left: -58px;
    display: none;
}
.background-btn-left-home2 {
    position: absolute;
    margin-top: -31px;
    margin-left: -55px;
    display: none;
}
.background-btn-bottom-home2 {
    position: absolute;
    margin-top: 9px;
    margin-left: -53px;
    display: none;
}
.btn-desktop:hover {
  .background-btn-left-home {
    display: inline-block;
  }
  .background-btn-bottom-home {
    display: inline-block;
  }
  .background-btn-left-home2 {
    display: inline-block;
  }
  .background-btn-bottom-home2 {
    display: inline-block;
  }
}


@media only screen and (max-width: 1470px) {
  .home-img-container {
    margin-left: 25%;
  }
}
@media only screen and (max-width: 1420px) {
  .home-img-container {
    margin-left: 10%;
  }
}
@media only screen and (max-width: 1220px) {
  .home-img-container {
    margin-left: 5%;
  }
}
@media only screen and (max-width: 1140px) {
  .home-img-container {
    margin-left: 0%;
  }
}
</style>
