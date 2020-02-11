<template>
    <div class="mobile">
        <!-- Slider Main Container -->
        <div class="swiper-container">
            <!-- Additional Required Wrapper -->
            <div class="swiper-wrapper">
                <!-- Slides -->
                <!-- Home -->
                <div id="home-mobile" class="swiper-slide home-mobile">
                    <div class="container-fluid home-mobile-container">
                        <div class="row no-gutter">
                            <div class="col">
                                <h1 class="font-heavy home-name">Don Brogdon,</h1>
                            </div>
                        </div>
                        <div class="row no-gutter">
                            <div class="col">
                                <h2 class="font-medium home-title">Developer<span class="animated-flash animated flash">_</span></h2>
                            </div>
                        </div>
                        <div class="row no-gutter">
                            <div class="col">
                                <p class="font-medium home-details"> I produce elegant, performant, and accessible digitial experiences.</p>
                            </div>
                        </div>
                        <div class="row no-gutter">
                            <div class="col">
                                <button class="btn-mobile" type="button" @click="goToSlide(2)"><span class="btn-text">Explore Work</span></button>
                                <span style="margin-right: 32px;"></span>
                                <button class="btn-mobile btn-outline-light btn-text" type="button" @click="goToSlide(1)"><span class="btn-text">View Profile</span></button>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- About -->
                <div id="about-mobile" class="swiper-slide about-mobile">
                    <div class="container-fluid">
                        <div class="row no-gutter">
                            <div class="col">
                                <h1>About</h1>
                            </div>
                        </div>
                        <div class="row no-gutter">
                            <div class="col">
                                <div class="profile-text-container font-medium">
                                    <p>Hello! I'm a Software Developer located in Norman, OK.</p>
                                    <p>I have exerience in leading teams, front-end, back-end, and UI/UX work.</p>
                                    <p>Browse some of my <button @click="goToSlide(2)" class="link-text" style="background-color: transparent; border: none; margin: -6px -6px -6px -6px;">work</button>, my <button @click="goToSlide(3)" class="link-text" style="background-color: transparent; border: none; margin: -6px -6px -6px -6px;">templates</button>, or <button @click="goToSlide(4)" class="link-text" style="background-color: transparent; border: none; margin: -6px -6px -6px -6px;">view my resume</button></p>
                                    <p>You can also find me at <a class="link-text" href="https://www.github.com/approximatelyinfinity">Github</a> or <a class="link-text" href="https://www.linkedin.com/in/donbrogdon">Linkedin</a></p>
                                </div>
                            </div>
                        </div>
                        <hr>
                        <div class="row no-gutter font-heavy">
                            <div class="col skills-container">
                                <h5><strong>Languages</strong></h5>
                                <div class="skills-list">
                                    <li v-for="(language, index) in languages" :key="`language-${index}`">
                                        <p class="skills-text">{{language}}</p>
                                    </li>
                                </div>
                            </div>
                            <div class="col skills-container">
                                <h5><strong>Frameworks</strong></h5>
                                <div class="skills-list">
                                    <li v-for="(framework, index) in frameworks" :key="`framework-${index}`">
                                        <p class="skills-text">{{framework}}</p>
                                    </li>
                                </div>
                            </div>
                            <div class="col skills-container">
                                <h5><strong>Tools</strong></h5>
                                <div class="skills-list">
                                    <li v-for="(tool, index) in tools" :key="`tool-${index}`">
                                        <p class="skills-text">{{tool}}</p>
                                    </li>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Projects -->
                <div id="projects-mobile" class="swiper-slide projects-mobile">
                    <div class="container-fluid">
                        <div class="row no-gutter">
                            <div class="col">
                                <h1 align="right">Projects</h1>
                            </div>
                        </div>
                        <div class="row no-gutter">
                            <div class="col">
                                <div class="project-container">
                                    <div class="project-background-img-mo">
                                        <h3 class="project-title">Melodic Odyssey</h3>
                                        <h6 class="project-stack">{{projects[0].stack}}</h6>
                                        <button class="btn-mobile" type="button"><a style="color: white" :href="projects[0].website">View</a></button>
                                    </div>
                                    <span class="project-background-left"></span>
                                    <span class="project-background-bottom"></span>
                                </div>
                            </div>
                        </div>
                        <div class="row no-gutter">
                            <div class="col">
                                <div class="project-container">
                                    <div class="project-background-img-cc">
                                        <h3 class="project-title">Candy Cane Shooter</h3>
                                        <h6 class="project-stack">{{projects[3].stack}}</h6>
                                        <button class="btn-mobile" type="button"><a style="color: white;" :href="projects[3].website">View</a></button>
                                    </div>
                                    <span class="project-background-left-2"></span>
                                    <span class="project-background-bottom-2"></span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Templates -->
                <div id="templates-mobile" class="swiper-slide templates-mobile">
                    <div class="container-fluid">
                        <div class="row no-gutter">
                            <div class="col">
                                <h1>Templates</h1>
                            </div>
                        </div>
                        <div class="row no-gutter">
                            <div class="col">
                                <div class="template-container">
                                    <div class="background-img">
                                        <div class="template-background">
                                            <h2 class="font-medium template-title">Dog Grooming</h2>
                                            <p class="template-stack">HTML/CSS, JS, Vue.js, Bootstrap</p>
                                            <button class="btn-outline-dark template-visit-btn" type="button">Visit</button> 

                                            <span class="template-background-left"></span>
                                            <span class="template-background-bottom"></span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="col">
                                <!--<div class="template-container">
                                    <div class="background-img">
                                        <div class="template-background">
                                            <h2 class="font-medium template-title">Dog Grooming</h2>
                                            <p class="template-stack">HTML/CSS, JS, Vue.js, Bootstrap</p>
                                            <button class="btn-outline-dark template-visit-btn" type="button">Visit</button> 

                                            <span class="template-background-left"></span>
                                            <span class="template-background-bottom"></span>
                                        </div>
                                    </div>
                                </div>-->
                            </div>
                        </div>
                        
                    </div>
                </div>

                <!-- Resume -->
                <div id="resume-mobile" class="swiper-slide resume-mobile">
                    <div class="container-fluid">
                        <div class="row no-gutter">
                            <div class="col">
                                <h1 align="right">Resume</h1>
                            </div>
                        </div>
                        <div class="row no-gutter">
                            <div class="col">
                                <div class="resume-container">
                                    <div class="resume-title">
                                        <h5>{{email}}</h5>
                                        <h5>{{location}} --- {{phone}}</h5>
                                        <button class="btn-mobile"><a href="http://www.donbrogdon.com/assets/CV.pdf" style="color: white;" download>View PDF</a></button>
                                        <span style="margin-left: 10px;"></span>
                                        <button class="btn-mobile" @click="goToSlide(5)"><a href="#" style="color: white;">Letters of Rec</a></button>
                                    </div>
                                    <hr/>
                                    <div class="row no-gutter">
                                        <div class="col">
                                            <div class="resume-education">
                                                <h4 class="resume-section">Education</h4>
                                                <div class="resume-education-container">
                                                    <h5 class="resume-headline">{{education[0].university}}</h5>
                                                    <p class="resume-text">{{education[0].degree}} in {{education[0].subject}} <span class="resume-date">--- {{education[0].date}}</span></p>
                                                    <p class="resume-text">{{education[1].degree}} in {{education[1].subject}}  <span class="resume-date">--- {{education[1].date}}</span></p>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="row no-gutter">
                                        <div class="col">
                                            <div class="resume-skills">
                                                <h4 class="resume-section">Skills</h4>
                                                <div class="resume-skills-container">
                                                    <div class="resume-skills-list">
                                                        <li v-for="(language, index) in languages" :key="`language-${index}`">
                                                            <p class="resume-skills-text"> - {{language}}</p>
                                                        </li>
                                                    </div>
                                                    <div class="resume-skills-list">
                                                        <li v-for="(framework, index) in frameworks" :key="`framework-${index}`">
                                                            <p class="resume-skills-text"> - {{framework}}</p>
                                                        </li>
                                                    </div>
                                                    <div class="resume-skills-list">
                                                        <li v-for="(tool, index) in tools" :key="`tool-${index}`">
                                                            <p class="resume-skills-text"> - {{tool}}</p>
                                                        </li>
                                                    </div>
                                                </div>
                                            </div>  
                                        </div>
                                    </div>

                                    <div class="row no-gutter">
                                        <div class="col">
                                            <div class="resume-projects">
                                                <h4 class="resume-section">Projects</h4>
                                                <div class="resume-projects-container">
                                                    <h5 class="resume-text">{{projects[0].subject}}</h5>
                                                    <p class="resume-text"><i>{{projects[0].role}}</i></p>
                                                    <p class="resume-text resume-text-details">{{projects[0].short}}</p>
                                                    <p class="resume-text resume-text-details-vs">{{projects[0].vs}}</p>
                                                </div>
                                                <br/>
                                                <div class="resume-projects-container">
                                                    <h5 class="resume-text">{{projects[1].subject}}</h5>
                                                    <p class="resume-text"><i>{{projects[1].role}}</i></p>
                                                    <p class="resume-text resume-text-details">{{projects[1].short}}</p>
                                                    <p class="resume-text resume-text-details-vs">{{projects[1].vs}}</p>
                                                </div>
                                                <br/>
                                                <div class="resume-projects-container">
                                                    <h5 class="resume-text">{{projects[2].subject}}</h5>
                                                    <p class="resume-text"><i>{{projects[2].role}}</i></p>
                                                    <p class="resume-text resume-text-details">{{projects[2].short}}</p>
                                                    <p class="resume-text resume-text-details-vs">{{projects[2].vs}}</p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col">
                                            <div class="resume-experience">
                                                <h4 class="resume-section">Experience</h4>
                                                <div class="resume-experience-container">
                                                    <h5 class="resume-text">{{workexp[0].company}}</h5>
                                                    <p class="resume-text"><i>{{workexp[0].title}}</i></p>
                                                    <p class="resume-text">{{workexp[0].from}} - {{workexp[0].to}}</p>
                                                    <p class="resume-text resume-text-details">{{workexp[0].short}}</p>
                                                </div>
                                                <br/>
                                                <div class="resume-experience-container">
                                                    <h5 class="resume-text">{{workexp[1].company}}</h5>
                                                    <p class="resume-text"><i>{{workexp[1].title}}</i></p>
                                                    <p class="resume-text">{{workexp[1].from}} - {{workexp[0].to}}</p>
                                                    <p class="resume-text resume-text-details">{{workexp[1].short}}</p>
                                                </div>
                                                <br/>
                                                <div class="resume-experience-container">
                                                    <h5 class="resume-text">{{workexp[2].subject}}</h5>
                                                    <p class="resume-text"><i>{{workexp[2].title}}</i></p>
                                                    <p class="resume-text">{{workexp[2].from}} - {{workexp[0].to}}</p>
                                                    <p class="resume-text resume-text-details">{{workexp[2].short}}</p>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Letter of Rec -->
                <div id="lor-mobile" class="swiper-slide lor-mobile">
                    <div class="container-fluid">
                        <div class="row no-gutter">
                            <div class="col">
                                <h1 align="right">Letters of Rec</h1>
                            </div>
                        </div>
                        <br/>
                        <div class="row no-gutter">
                            <div class="col">
                                <img height="175px" src="../assets/DoDseal.png"/>
                                <br/>
                                <a class="pdf-link" href="http://www.donbrogdon.com/assets/DoD.pdf" target="_blank">
                                    <svg class="download-btn" height="32pt" viewBox="0 0 512 512" width="32pt" xmlns="http://www.w3.org/2000/svg" fill="white">
                                        <path d="m409.785156 278.5-153.785156 153.785156-153.785156-153.785156 28.285156-28.285156 105.5 105.5v-355.714844h40v355.714844l105.5-105.5zm102.214844 193.5h-512v40h512zm0 0"/>
                                    </svg>
                                    <p style="display: inline-block; margin-left: 4px; color: white;">Download</p>
                                </a>
                            </div>
                        </div>
                        <br/><br/>
                        <div class="row no-gutter">
                            <div class="col">
                                <h1><strong>BMT</strong></h1>
                                <a class="pdf-link" href="http://www.donbrogdon.com/assets/BMT.pdf" target="_blank">
                                    <svg class="download-btn" height="32pt" viewBox="0 0 512 512" width="32pt" xmlns="http://www.w3.org/2000/svg" fill="white">
                                        <path d="m409.785156 278.5-153.785156 153.785156-153.785156-153.785156 28.285156-28.285156 105.5 105.5v-355.714844h40v355.714844l105.5-105.5zm102.214844 193.5h-512v40h512zm0 0"/>
                                    </svg>
                                    <p style="display: inline-block; margin-left: 4px; color: white;">Download</p>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>

            </div>    
        </div>
        <!-- navigation buttons -->
        <div class="arrow-container">
            <div class="swiper-button-prev"></div>
            <div class="swiper-button-next"></div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Mobile",
    props: {
      location: {
          type: String
      },
      phone: {
          type: String
      },
      email: {
          type: String
      },
      workexp: {
          type: Array
      },
      education: {
          type: Array
      },
      languages: {
          type: Array
      },
      frameworks: {
          type: Array
      },
      tools: {
          type: Array
      },
      projects: {
          type: Array
      },
    },
    data() {
        return {
            swiper: null,
            displayState: true
        }
    },
    mounted() {
    this.swiper = new window.Swiper('.swiper-container', {
      effect: 'cube',
      grabCursor: true,
      cubeEffect: {
        shadow: false,
        slideShadows: false,
        shadowOffset: 20,
        shadowScale: 0.94,
      },
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev'
      }
    })
  },
  methods: {
      goToSlide: function(slide) {
          this.swiper.slideTo(slide);
      },
      display: function(e) {
          e.prventDefault()
      }
  },
}
</script>

<style scoped lang="scss">
@import './src/style/globals.scss';
@import './src/style/fonts.scss';
.mobile {
    background-color: black;
    overflow-x: hidden;
}

.home-mobile {
        background-image: url('../assets/home.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        color: white;

        .animated-flash {
            animation-iteration-count: infinite;
        }
        .home-mobile-container {
            margin-top: 34%;
        }

        .home-name {
            font-size: 98px;
        }

        .home-title {
            font-size: 52px;
            margin-left: 1%;
        }

        .home-details {
            font-size: 32px;
            margin-left: 1%;
        }
    }

    .about-mobile {
        color: white;
        text-align: right;
        background-image: url('../assets/2.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        font-size: 22px;

        .link-text {
             color: map-get($colors, primary-dark);
        }

        .skills-container {
            margin-top: 6%;
            text-align: right;
            height: 100px;
        }
        

        .skills-text {
            margin-top: -10px;
        }
    }

.projects-mobile {
    background-image: url('../assets/2.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    color: white;

    .btn-mobile {
        padding: 4px 4px 4px 4px;
        margin-left: 12px;
    }

    .project-container {
        margin-top: 28px;
    }
    .project-background-img-mo {
        height: 120px;
        width: 100%;
        margin-top: 5px;
        margin-left: 5px;
        background: rgba(0, 0, 0, 0.5);
        /*background: rgb(82,7,170);
        background: -moz-linear-gradient(220deg, rgba(82,7,170,1) 0%, rgba(110,30,203,1) 25%, rgba(227,182,94,1) 100%);
        background: -webkit-linear-gradient(220deg, rgba(82,7,170,1) 0%, rgba(110,30,203,1) 25%, rgba(227,182,94,1) 100%);
        background: linear-gradient(220deg, rgba(82,7,170,1) 0%, rgba(110,30,203,1) 25%, rgba(227,182,94,1) 100%);
        filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#5207aa",endColorstr="#e3b65e",GradientType=1);*/
    }
    .project-background-img-cc {
        height: 120px;
        width: 100%;
        margin-top: 5px;
        margin-left: 5px;
        background: rgba(0, 0, 0, 0.5);
        /*background: rgb(16,130,21);
        background: -moz-linear-gradient(229deg, rgba(16,130,21,1) 0%, rgba(108,113,0,1) 50%, rgba(251,5,5,1) 100%);
        background: -webkit-linear-gradient(229deg, rgba(16,130,21,1) 0%, rgba(108,113,0,1) 50%, rgba(251,5,5,1) 100%);
        background: linear-gradient(229deg, rgba(16,130,21,1) 0%, rgba(108,113,0,1) 50%, rgba(251,5,5,1) 100%);
        filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#108215",endColorstr="#fb0505",GradientType=1);*/
    }
    .project-title {
        margin-left: 10px;
    }
    .project-stack {
        margin-top: -4px;
        margin-left: 12px;
    }

    .project-background-left {
        width: 10px;
        height: 120px;
        background-color: map-get($colors, primary);
        position: absolute;
        transform: skewY(-45deg);
        margin-top: -115px;
        margin-left: -5px;
    }

    .project-background-bottom {
        width: 96.2%;
        height: 10px;
        background-color: map-get($colors, primary);
        position: absolute;
        margin-top: 0px;
        margin-left: 0px;
        transform: skewX(-42deg);
    }
}
.templates-mobile {
    background-color: green;

    .background-img {
        position: relative;
        margin-top: 30px;
    }

    .background-img:hover {
        span {
            display: inline-block;
        }
    }

    /*.template-background {
        height: 220px;
        width: 220px;
        background-image: url('../assets/dog.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        position: absolute;
    }*/

    .template-background/*:hover*/ {
        height: 220px;
        width: 220px;
        margin-left: 10px;
        margin-top: -5px;
        background: rgb(236,107,143);
        background: -moz-linear-gradient(60deg, rgba(236,107,143,1) 25%, rgba(148,186,38,1) 75%);
        background: -webkit-linear-gradient(60deg, rgba(236,107,143,1) 25%, rgba(148,186,38,1) 75%);
        background: linear-gradient(60deg, rgba(236,107,143,1) 25%, rgba(148,186,38,1) 75%);
        filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#ec6b8f",endColorstr="#94ba26",GradientType=1);

        /*.template-title {
            display: block;
        }
        .template-stack {
            display: block;
        }
        .template-visit-btn {
            display: block;
        }*/
    }

    .template-title {
        color: white;
        border-bottom: 1px solid white;
        margin-left: 10px;
        //display: none;
    }
    .template-background-left {
        width: 10px;
        height: 220px;
        background-color: map-get($colors, accent);
        position: absolute;
        transform: skewY(-40deg);
        margin-top: -43px;
        margin-left: -10px;
        //display: none;
    }
    .template-background-bottom {
        width: 220px;
        height: 10px;
        background-color: map-get($colors,accent);
        position: absolute;
        margin-top: 172px;
        margin-left: -5.5px;
        transform: skewX(-49deg);
        //display: none;
    }

    .template-stack {
        color: white;
        position: absolute;
        margin-left: 10px;
        //display: none;
    }

    .template-visit-btn {
        margin-left: 16px;
        margin-top: 55px;
        position: absolute;
        border: 1px solid white;
        background: transparent;
        //display: none;
    }

    .template-background-btn-left {
        margin-top: 187px;
        margin-left: 12px;
        position: absolute;
        display: none;
    }
    .template-background-btn-bottom {
        margin-top: 225px;
        margin-left: 14px;
        position: absolute;
        display: none;
    }
}
.resume-mobile {
    background-color: pink;
    color: white;

    .btn-mobile {
        padding: 4px 4px 4px 4px;
    }
    li {
        display: inline;
    }
    .resume-date {
        display: inline;
        font-style: italic;
    }
    .resume-skills-text {
        display: inline;
    }
    .resume-title {
        text-align: right;
    }
    .resume-text-title {
        margin-bottom: 14px;
    }
    .resume-text {
        margin-top: -8px;
        margin-bottom: 4px;
    }
    .resume-text-details {
        display: block;
    }
    .resume-text-details-vs {
        display: none;
    }
}

.lor-mobile {
    color: white;
    background-image: url('../assets/7.jpg');
    background-repeat: no-repeat;
    background-size: cover;

}

.swiper-slide {
    min-height: calc(100vh - 70px);
}

.arrow-container {
    background-color: black;
    height: 70px;
    position: relative;
    z-index: 1;
    
    .swiper-button-prev {
        color: white;
    }

    .swiper-button-next {
        color: white;
    }
}

//iPad
@media only screen and (max-height: 1024px) {
    .home-mobile {
        background-image: url('../assets/home.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        color: white;

        .home-mobile-container {
            margin-top: 34%;
        }

        .home-name {
            font-size: 98px;
        }

        .home-title {
            font-size: 52px;
            margin-left: 1%;
        }

        .home-details {
            font-size: 32px;
            margin-left: 1%;
        }
    }

    .about-mobile {
        background-image: url('../assets/6.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        color: white;
        text-align: right;
        font-size: 24px;

        .link-text {
             color: map-get($colors, primary-dark);
        }

        .skills-container {
            margin-top: 6%;
            text-align: right;
            background: rgba(0, 0, 0, 0.5);
            height: 575px;

            h5 {
                font-size: 26px;
            }
        }

        .skills-text {
            margin-top: -10px;
        }
    }

    .projects-mobile {
        background-image: url('../assets/2.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        color: white;

    .btn-mobile {
        padding: 4px 4px 4px 4px;
        margin-left: 12px;
    }

    .project-container {
        margin-top: 28px;
    }
    .project-background-img-mo {
        height: 120px;
        width: 100%;
        margin-top: 5px;
        margin-left: 5px;
        background: rgba(0, 0, 0, 0.5);
        /*background: rgb(82,7,170);
        background: -moz-linear-gradient(220deg, rgba(82,7,170,1) 0%, rgba(110,30,203,1) 25%, rgba(227,182,94,1) 100%);
        background: -webkit-linear-gradient(220deg, rgba(82,7,170,1) 0%, rgba(110,30,203,1) 25%, rgba(227,182,94,1) 100%);
        background: linear-gradient(220deg, rgba(82,7,170,1) 0%, rgba(110,30,203,1) 25%, rgba(227,182,94,1) 100%);
        filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#5207aa",endColorstr="#e3b65e",GradientType=1);*/
    }
    .project-background-img-cc {
        height: 120px;
        width: 100%;
        margin-top: 5px;
        margin-left: 5px;
        background: rgba(0, 0, 0, 0.5);
        /*background: rgb(16,130,21);
        background: -moz-linear-gradient(229deg, rgba(16,130,21,1) 0%, rgba(108,113,0,1) 50%, rgba(251,5,5,1) 100%);
        background: -webkit-linear-gradient(229deg, rgba(16,130,21,1) 0%, rgba(108,113,0,1) 50%, rgba(251,5,5,1) 100%);
        background: linear-gradient(229deg, rgba(16,130,21,1) 0%, rgba(108,113,0,1) 50%, rgba(251,5,5,1) 100%);
        filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#108215",endColorstr="#fb0505",GradientType=1);*/
    }
    .project-title {
        margin-left: 10px;
    }
    .project-stack {
        margin-top: -4px;
        margin-left: 12px;
    }

    .project-background-left {
        width: 10px;
        height: 120px;
        background-color: map-get($colors, primary);
        position: absolute;
        transform: skewY(-45deg);
        margin-top: -115px;
        margin-left: -5px;
    }

    .project-background-bottom {
        width: 96.2%;
        height: 10px;
        background-color: map-get($colors, primary);
        position: absolute;
        margin-top: 0px;
        margin-left: 0px;
        transform: skewX(-42deg);
    }

    .project-background-left-2 {
        width: 10px;
        height: 120px;
        background-color: map-get($colors, secondary);
        position: absolute;
        transform: skewY(-45deg);
        margin-top: -115px;
        margin-left: -5px;
    }

    .project-background-bottom-2 {
        width: 96.2%;
        height: 10px;
        background-color: map-get($colors, secondary);
        position: absolute;
        margin-top: 0px;
        margin-left: 0px;
        transform: skewX(-42deg);
    }
}

    .templates-mobile {
        background-image: url('../assets/3.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        color: white;
        h1 {
            text-align: right;
        }

    .background-img {
        position: relative;
        margin-top: 30px;
    }

    .background-img:hover {
        span {
            display: inline-block;
        }
    }

    /*.template-background {
        height: 220px;
        width: 220px;
        background-image: url('../assets/dog.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        position: absolute;
    }*/

    .template-background/*:hover*/ {
        height: 220px;
        width: 220px;
        margin-left: 10px;
        margin-top: -5px;
        background: rgba(0, 0, 0, 0.5);
        /*background: rgb(236,107,143);
        background: -moz-linear-gradient(60deg, rgba(236,107,143,1) 25%, rgba(148,186,38,1) 75%);
        background: -webkit-linear-gradient(60deg, rgba(236,107,143,1) 25%, rgba(148,186,38,1) 75%);
        background: linear-gradient(60deg, rgba(236,107,143,1) 25%, rgba(148,186,38,1) 75%);
        filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#ec6b8f",endColorstr="#94ba26",GradientType=1);*/

        /*.template-title {
            display: block;
        }
        .template-stack {
            display: block;
        }
        .template-visit-btn {
            display: block;
        }*/
    }

    .template-title {
        color: white;
        border-bottom: 1px solid white;
        margin-left: 10px;
        //display: none;
    }
    .template-background-left {
        width: 10px;
        height: 220px;
        background-color: map-get($colors, accent);
        position: absolute;
        transform: skewY(-40deg);
        margin-top: -43px;
        margin-left: -10px;
        //display: none;
    }
    .template-background-bottom {
        width: 220px;
        height: 10px;
        background-color: map-get($colors,accent);
        position: absolute;
        margin-top: 172px;
        margin-left: -5.5px;
        transform: skewX(-49deg);
        //display: none;
    }

    .template-stack {
        color: white;
        position: absolute;
        margin-left: 10px;
        //display: none;
    }

    .template-visit-btn {
        margin-left: 16px;
        margin-top: 55px;
        position: absolute;
        border: 1px solid white;
        background: transparent;
        //display: none;
    }

    .template-background-btn-left {
        margin-top: 187px;
        margin-left: 12px;
        position: absolute;
        display: none;
    }
    .template-background-btn-bottom {
        margin-top: 225px;
        margin-left: 14px;
        position: absolute;
        display: none;
    }
}

    .resume-mobile {
        background-image: url('../assets/5.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        color: white;

    .btn-mobile {
        padding: 4px 4px 4px 4px;
    }
    li {
        display: inline;
    }
    .resume-date {
        display: inline;
        font-style: italic;
    }
    .resume-skills-text {
        display: inline;
    }
    .resume-title {
        text-align: right;
    }
    .resume-text-title {
        margin-bottom: 14px;
    }
    .resume-text {
        margin-top: -8px;
        margin-bottom: 4px;
    }
    .resume-text-details {
        display: block;
    }
    .resume-text-details-vs {
        display: none;
    }
}
}

//iPhone X
@media only screen and (max-height: 812px) {
    .home-mobile {
        background-image: url('../assets/home.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        color: white;

        .home-mobile-container {
            margin-top: 40%;
        }

        .home-name {
            font-size: 56px;
        }

        .home-title {
            font-size: 44px;
            margin-left: 1%;
        }

        .home-details {
            font-size: 28px;
            margin-left: 1%;
        }
    }

    .about-mobile {
        color: white;
        text-align: right;
        font-size: 20px;

        .link-text {
             color: map-get($colors, primary-dark);
        }

        .skills-container {
            margin-top: 20px;
            text-align: center;
            height: 329px;
            
            h5 {
                font-size: 20px;
            }

        }
        
        .skills-text {
            margin-top: -10px;
            font-size: 16px;
        }
    }

    .projects-mobile {
        .project-background-bottom {
            width: 92.5%;
        }
        .project-background-bottom {
            width: 92.2%;
        }
        .project-background-bottom-2 {
            width: 92.2%;;
        }
    }

    .templates-mobile {

        .template-background {
            height: 140px;
            width: 140px;
        }

        .template-background:hover {
            margin-left: 0px;
            margin-top: -5px;
        }

        .template-title {
            font-size: 20px;
        }
        .template-background-left {
            width: 6px;
            height: 140px;
            margin-top: -30px;
            margin-left: -6px;
        }
        .template-background-bottom {
            width: 140px;
            height: 6px;
            margin-top: 107px;
            margin-left: -3px;
        }

        .template-stack {
            font-size: 14px;
        }

        .template-visit-btn {
            margin-left: 16px;
            margin-top: 55px;
        }
    }

    .resume-mobile {
        background-color: orange;
        color: white;

        .btn-mobile {
            padding: 4px 4px 4px 4px;
        }

        .resume-title {
            text-align: right;

            h5 {
                font-size: 16px;
            }
        }
        .resume-text-title {
            margin-bottom: 14px;
        }
        .resume-text {
            margin-top: -8px;
            margin-bottom: 4px;
            font-size: 14px;
        }
        .resume-section {
            font-size: 20px;
        }
        .resume-headline {
            font-size: 16px;
        }
        .resume-date {
            display: none;
        }
        .resume-skills-text {
            font-size: 14px;
        }
        .resume-skills-list {
            margin-bottom: -6px;
        }
        .resume-projects {
            margin-top: 12px;
        }
        .resume-experience {
            margin-top: 12px;
        }
        .resume-text-details {
            display: none;
            margin-bottom: 0px;
        }
        .resume-text-details-vs {
            display: block;
            margin-bottom: 4px;
        }
    } 
}

//iPhone 8 Plus
@media only screen and (max-height: 736px) {
    .home-mobile {
        background-image: url('../assets/home.jpg');
        background-repeat: no-repeat;
        background-size: cover;

        .home-mobile-container {
            margin-top: 40%;
        }

        .home-name {
            font-size: 62px;
        }

        .home-title {
            font-size: 42px;
            margin-left: 1%;
        }

        .home-details {
            font-size: 22px;
            margin-left: 1%;
        }
    }

    .about-mobile {
        text-align: right;
        color: white;
        background-size: 700px;
        height: 319px;

        hr {
            display: none;
        }

        .link-text {
             color: map-get($colors, primary-dark);
        }

        .skills-container {
            margin-top: 20px;
            text-align: center;

            h5 {
                font-size: 18px;
            }
        }
        
        .skills-text {
            margin-top: -10px;
        }
    }

    .projects-mobile {
        .project-background-bottom {
            width: 93%;
        }
    }

    .templates-mobile {
        background-color: green;

        .template-background {
            height: 140px;
            width: 140px;
        }

        .template-background:hover {
            margin-left: 0px;
            margin-top: -5px;
        }

        .template-title {
            font-size: 20px;
        }
        .template-background-left {
            width: 6px;
            height: 140px;
            margin-top: -30px;
            margin-left: -6px;
        }
        .template-background-bottom {
            width: 140px;
            height: 6px;
            margin-top: 107px;
            margin-left: -3px;
        }

        .template-stack {
            font-size: 14px;
        }

        .template-visit-btn {
            margin-left: 16px;
            margin-top: 55px;
        }
    }

    .resume-mobile {
        background-color: green;
        color: white;
        hr {
            display: none;
        }
        br {
            display: none;
        }
        .btn-mobile {
            padding: 4px 4px 4px 4px;
        }

        .resume-title {
            text-align: right;

            h5 {
                font-size: 15px;
            }
        }
        .resume-text-title {
            margin-bottom: 14px;
        }
        .resume-text {
            margin-top: -8px;
            margin-bottom: 4px;
            font-size: 14px;
        }
        .resume-section {
            font-size: 20px;
        }
        .resume-headline {
            font-size: 16px;
        }
        .resume-date {
            display: none;
        }
        .resume-skills-text {
            font-size: 14px;
        }
        .resume-skills-list {
            margin-bottom: -6px;
        }
        .resume-projects {
            margin-top: 12px;
        }
        .resume-experience {
            margin-top: 12px;
        }
        .resume-text-details {
            display: none;
            margin-bottom: 0px;
        }
        .resume-text-details-vs {
            display: block;
            margin-bottom: 4px;
        }
        .resume-projects-container {
            padding-bottom: 4px;
        }
        .resume-experience-container {
            padding-bottom: 12px;
        }
    } 
}

//iPhone 8
@media only screen and (max-height: 667px) {
    .home-mobile {
        .home-mobile-container {
            margin-top: 40%;
        }

        .home-name {
            font-size: 52px;
        }

        .home-title {
            font-size: 42px;
            margin-left: 1%;
        }

        .home-details {
            font-size: 22px;
            margin-left: 1%;
        }
    }

    .about-mobile {
        text-align: right;
        font-size: 16px;
        height: 309px;

        br {
            display: none;
        }

        .link-text {
             color: map-get($colors, primary-dark);
        }

        .skills-container {
            margin-top: 20px;
            text-align: center;
            font-size: 16px;
        }
        
        .skills-text {
            margin-top: -10px;
        }
    }

    .projects-mobile {
        .project-background-bottom {
            width: 92.3%;
        }
    }

    .templates-mobile {
        background-color: green;

        .template-background {
            height: 140px;
            width: 140px;
        }

        .template-background:hover {
            margin-left: 0px;
            margin-top: -5px;
        }

        .template-title {
            font-size: 20px;
        }
        .template-background-left {
            width: 6px;
            height: 140px;
            margin-top: -30px;
            margin-left: -6px;
        }
        .template-background-bottom {
            width: 140px;
            height: 6px;
            margin-top: 107px;
            margin-left: -3px;
        }

        .template-stack {
            font-size: 14px;
        }

        .template-visit-btn {
            margin-left: 16px;
            margin-top: 55px;
        }
    }

    .resume-mobile {
        background-color: green;
        color: white;
        hr {
            display: none;
        }
        br {
            display: none;
        }
        .btn-mobile {
            padding: 4px 4px 4px 4px;
        }

        .resume-title {
            text-align: right;
            height: 55px;
            z-index: 1;

            h5 {
                font-size: 15px;
            }
        }
        .resume-text-title {
            margin-bottom: 14px;
        }
        .resume-text {
            margin-top: -8px;
            margin-bottom: 4px;
            font-size: 14px;
        }
        .resume-section {
            font-size: 20px;
        }
        .resume-headline {
            font-size: 16px;
        }
        .resume-date {
            display: none;
        }
        .resume-skills-text {
            font-size: 14px;
        }
        .resume-skills-list {
            margin-bottom: -6px;
        }
        .resume-projects {
            margin-top: 12px;
        }
        .resume-experience {
            margin-top: 12px;
        }
        .resume-text-details {
            display: none;
            margin-bottom: 0px;
        }
        .resume-text-details-vs {
            display: block;
            margin-bottom: 4px;
        }
        .resume-projects-container {
            padding-bottom: 2px;
        }
        .resume-experience-container {
            padding-bottom: 12px;
        }
        .resume-education-container {
            margin-top: -10px;
        }
        .resume-skills-container {
            margin-top: -10px;
        }
    }
}

//Android 
@media only screen and (max-height: 640px) {
    .home-mobile {
        color: white;

        .home-mobile-container {
            margin-top: 40%;
        }

        .home-name {
            font-size: 42px;
        }

        .home-title {
            font-size: 32px;
            margin-left: 1%;
        }

        .home-details {
            font-size: 16px;
            margin-left: 1%;
        }
    }

    .about-mobile {
        text-align: right;

        .link-text {
             color: map-get($colors, primary-dark);
        }

        .skills-container {
            text-align: center;
            display: inline;
            font-size: 13px;
        }
        
        .skills-text {
            margin-top: -8px;
        }
    }

    .projects-mobile {
        .project-background-bottom {
            width: 92%;
        }
    }

    .templates-mobile {
        background-color: green;

        .template-background {
            height: 140px;
            width: 140px;
        }

        .template-background:hover {
            margin-left: 0px;
            margin-top: -5px;
        }

        .template-title {
            font-size: 20px;
        }
        .template-background-left {
            width: 6px;
            height: 140px;
            margin-top: -30px;
            margin-left: -6px;
        }
        .template-background-bottom {
            width: 140px;
            height: 6px;
            margin-top: 107px;
            margin-left: -3px;
        }

        .template-stack {
            font-size: 14px;
        }

        .template-visit-btn {
            margin-left: 16px;
            margin-top: 55px;
        }
    }

    .resume-mobile {
        background-color: green;
        color: white;
        hr {
            display: none;
        }
        br {
            display: none;
        }
        .btn-mobile {
            padding: 3px 3px 3px 3px;
        }

        .resume-title {
            text-align: right;
            height: 55px;
            z-index: 1;

            h5 {
                font-size: 14px;
            }
        }
        .resume-text-title {
            margin-bottom: 14px;
        }
        .resume-text {
            margin-top: -8px;
            margin-bottom: 4px;
            font-size: 14px;
        }
        .resume-section {
            font-size: 18px;
        }
        .resume-headline {
            font-size: 14px;
        }
        .resume-date {
            display: none;
        }
        .resume-skills-text {
            font-size: 14px;
        }
        .resume-skills-list {
            margin-bottom: -6px;
        }
        .resume-projects {
            margin-top: 12px;
        }
        .resume-experience {
            margin-top: 12px;
        }
        .resume-text-details {
            display: none;
            margin-bottom: 0px;
        }
        .resume-text-details-vs {
            display: block;
            margin-bottom: 4px;
        }
        .resume-education-container {
            margin-top: -12px;
        }
        .resume-skills-container {
            margin-top: -12px;
        }
    }
}

//iPhone 5
@media only screen and (max-height: 568px) {
    .btn-mobile {
        padding: 10px 10px 10px 10px;
    }

    .home-mobile {

        .home-mobile-container {
            margin-top: 35%;
        }

        .home-name {
            font-size: 42px;
        }

        .home-title {
            font-size: 32px;
            margin-left: 1%;
        }

        .home-details {
            font-size: 16px;
            margin-left: 1%;
        }
    }

    .about-mobile {
        text-align: right;
        font-size: 16px;

        .link-text {
             color: map-get($colors, primary-dark);
        }

        .skills-container {
            margin-top: 0px;
            text-align: center;
            width: 60px;
            display: none;
        }
        
        .skills-text {
            margin-top: -12px;
        }
    }

    .projects-mobile {
        .project-background-bottom {
            width: 91%;
        }
    }

    .templates-mobile {
        background-color: green;

        .template-background {
            height: 140px;
            width: 140px;
        }

        .template-background:hover {
            margin-left: 0px;
            margin-top: -5px;
        }

        .template-title {
            font-size: 20px;
        }
        .template-background-left {
            width: 6px;
            height: 140px;
            margin-top: -30px;
            margin-left: -6px;
        }
        .template-background-bottom {
            width: 140px;
            height: 6px;
            margin-top: 107px;
            margin-left: -3px;
        }

        .template-stack {
            font-size: 14px;
        }

        .template-visit-btn {
            margin-left: 16px;
            margin-top: 55px;
        }
    }

    .resume-mobile {
        color: white;
        hr {
            display: none;
        }
        br {
            display: none;
        }
        .btn-mobile {
            padding: 3px 3px 3px 3px;
        }

        .resume-title {
            text-align: right;
            height: 55px;
            z-index: 1;

            h5 {
                font-size: 14px;
            }
        }
        .resume-education {
            margin-top: 30px;
        }
        .resume-projects {
            display: none;
        }
        .resume-experience {
            display: none;
        }
        .resume-text-title {
            margin-bottom: 14px;
        }
        .resume-text {
            margin-top: -8px;
            margin-bottom: 4px;
            font-size: 14px;
        }
        .resume-section {
            font-size: 18px;
        }
        .resume-headline {
            font-size: 14px;
        }
        .resume-date {
            display: none;
        }
        .resume-skills-text {
            font-size: 14px;
        }
        .resume-skills-list {
            margin-bottom: -6px;
        }
        .resume-projects {
            margin-top: 12px;
        }
        .resume-experience {
            margin-top: 12px;
        }
        .resume-text-details {
            display: none;
            margin-bottom: 0px;
        }
        .resume-text-details-vs {
            display: block;
            margin-bottom: 4px;
        }
        .resume-education-container {
            margin-top: -12px;
        }
        .resume-skills-container {
            margin-top: -12px;
        }
    }
}
</style>