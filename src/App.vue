<template>
  <div id="app">
    <div v-if="window.width < 910">
      <Mobile :location="location" :phone="phone" :email="email" :workexp="workexp" :education="education" :languages="languages" :frameworks="frameworks" :tools="tools" :projects="projects"/>
    </div>
    <div v-else>
      <div class="navigation">
        <nav class="navbar">
          <button v-on:click="burger()" id="btn-menu" class="btn-menu ml-auto" type="button">
            <span class="burger-icon"></span>
          </button>
        </nav>
      </div>
      <nav id="menu" class="menu ml-auto">
        <ul class="list-unstyled">
          <!-- Home -->
          <router-link to="/">
            <li class="list-item">
              <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="Capa_1" x="0px" y="0px" viewBox="0 0 512.001 512.001" style="enable-background:new 0 0 512.001 512.001;" xml:space="preserve" class="nav-item">
                <g>
                  <path d="M503.402,228.885L273.684,19.567c-10.083-9.189-25.288-9.188-35.367-0.001L8.598,228.886    c-8.077,7.36-10.745,18.7-6.799,28.889c3.947,10.189,13.557,16.772,24.484,16.772h36.69v209.721    c0,8.315,6.742,15.057,15.057,15.057h125.914c8.315,0,15.057-6.741,15.057-15.057V356.932h74.002v127.337    c0,8.315,6.742,15.057,15.057,15.057h125.908c8.315,0,15.057-6.741,15.057-15.057V274.547h36.697    c10.926,0,20.537-6.584,24.484-16.772C514.147,247.585,511.479,236.246,503.402,228.885z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#FFFFFF"/>
                </g>
                <g>
                  <path d="M445.092,42.73H343.973l116.176,105.636v-90.58C460.149,49.471,453.408,42.73,445.092,42.73z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#FFFFFF"/>
                </g>
              </svg>
            </li>
          </router-link>
          <!-- About -->
          <router-link to="/about" :phone="phone">
            <li class="list-item">
              <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="Capa_1" x="0px" y="0px" viewBox="0 0 482.9 482.9" style="enable-background:new 0 0 482.9 482.9;" xml:space="preserve" class="nav-item">
                <g>
                  <path d="M239.7,260.2c0.5,0,1,0,1.6,0c0.2,0,0.4,0,0.6,0c0.3,0,0.7,0,1,0c29.3-0.5,53-10.8,70.5-30.5    c38.5-43.4,32.1-117.8,31.4-124.9c-2.5-53.3-27.7-78.8-48.5-90.7C280.8,5.2,262.7,0.4,242.5,0h-0.7c-0.1,0-0.3,0-0.4,0h-0.6    c-11.1,0-32.9,1.8-53.8,13.7c-21,11.9-46.6,37.4-49.1,91.1c-0.7,7.1-7.1,81.5,31.4,124.9C186.7,249.4,210.4,259.7,239.7,260.2z     M164.6,107.3c0-0.3,0.1-0.6,0.1-0.8c3.3-71.7,54.2-79.4,76-79.4h0.4c0.2,0,0.5,0,0.8,0c27,0.6,72.9,11.6,76,79.4    c0,0.3,0,0.6,0.1,0.8c0.1,0.7,7.1,68.7-24.7,104.5c-12.6,14.2-29.4,21.2-51.5,21.4c-0.2,0-0.3,0-0.5,0l0,0c-0.2,0-0.3,0-0.5,0    c-22-0.2-38.9-7.2-51.4-21.4C157.7,176.2,164.5,107.9,164.6,107.3z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#FFFFFF"/>
                  <path d="M446.8,383.6c0-0.1,0-0.2,0-0.3c0-0.8-0.1-1.6-0.1-2.5c-0.6-19.8-1.9-66.1-45.3-80.9c-0.3-0.1-0.7-0.2-1-0.3    c-45.1-11.5-82.6-37.5-83-37.8c-6.1-4.3-14.5-2.8-18.8,3.3c-4.3,6.1-2.8,14.5,3.3,18.8c1.7,1.2,41.5,28.9,91.3,41.7    c23.3,8.3,25.9,33.2,26.6,56c0,0.9,0,1.7,0.1,2.5c0.1,9-0.5,22.9-2.1,30.9c-16.2,9.2-79.7,41-176.3,41    c-96.2,0-160.1-31.9-176.4-41.1c-1.6-8-2.3-21.9-2.1-30.9c0-0.8,0.1-1.6,0.1-2.5c0.7-22.8,3.3-47.7,26.6-56    c49.8-12.8,89.6-40.6,91.3-41.7c6.1-4.3,7.6-12.7,3.3-18.8c-4.3-6.1-12.7-7.6-18.8-3.3c-0.4,0.3-37.7,26.3-83,37.8    c-0.4,0.1-0.7,0.2-1,0.3c-43.4,14.9-44.7,61.2-45.3,80.9c0,0.9,0,1.7-0.1,2.5c0,0.1,0,0.2,0,0.3c-0.1,5.2-0.2,31.9,5.1,45.3    c1,2.6,2.8,4.8,5.2,6.3c3,2,74.9,47.8,195.2,47.8s192.2-45.9,195.2-47.8c2.3-1.5,4.2-3.7,5.2-6.3    C447,415.5,446.9,388.8,446.8,383.6z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#FFFFFF"/>
                </g>
              </svg>
            </li>
          </router-link>
          <!-- Projects -->
          <router-link to="/projects">
            <li class="list-item">
              <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="Capa_1" x="0px" y="0px" viewBox="0 0 522.468 522.469" style="enable-background:new 0 0 522.468 522.469;" xml:space="preserve" class="nav-item">
                <g>
                  <path d="M325.762,70.513l-17.706-4.854c-2.279-0.76-4.524-0.521-6.707,0.715c-2.19,1.237-3.669,3.094-4.429,5.568L190.426,440.53    c-0.76,2.475-0.522,4.809,0.715,6.995c1.237,2.19,3.09,3.665,5.568,4.425l17.701,4.856c2.284,0.766,4.521,0.526,6.71-0.712    c2.19-1.243,3.666-3.094,4.425-5.564L332.042,81.936c0.759-2.474,0.523-4.808-0.716-6.999    C330.088,72.747,328.237,71.272,325.762,70.513z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#FFFFFF"/>
                  <path d="M166.167,142.465c0-2.474-0.953-4.665-2.856-6.567l-14.277-14.276c-1.903-1.903-4.093-2.857-6.567-2.857    s-4.665,0.955-6.567,2.857L2.856,254.666C0.95,256.569,0,258.759,0,261.233c0,2.474,0.953,4.664,2.856,6.566l133.043,133.044    c1.902,1.906,4.089,2.854,6.567,2.854s4.665-0.951,6.567-2.854l14.277-14.268c1.903-1.902,2.856-4.093,2.856-6.57    c0-2.471-0.953-4.661-2.856-6.563L51.107,261.233l112.204-112.201C165.217,147.13,166.167,144.939,166.167,142.465z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#FFFFFF"/>
                  <path d="M519.614,254.663L386.567,121.619c-1.902-1.902-4.093-2.857-6.563-2.857c-2.478,0-4.661,0.955-6.57,2.857l-14.271,14.275    c-1.902,1.903-2.851,4.09-2.851,6.567s0.948,4.665,2.851,6.567l112.206,112.204L359.163,373.442    c-1.902,1.902-2.851,4.093-2.851,6.563c0,2.478,0.948,4.668,2.851,6.57l14.271,14.268c1.909,1.906,4.093,2.854,6.57,2.854    c2.471,0,4.661-0.951,6.563-2.854L519.614,267.8c1.903-1.902,2.854-4.096,2.854-6.57    C522.468,258.755,521.517,256.565,519.614,254.663z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#FFFFFF"/>
                </g> 
              </svg>
            </li>
          </router-link>
          <!-- Templates -->
          <router-link to="/templates">
            <li class="list-item">
              <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="Capa_1" x="0px" y="0px" viewBox="0 0 548.172 548.172" style="enable-background:new 0 0 548.172 548.172;" xml:space="preserve" class="nav-item">
                <g>
                  <path d="M534.75,49.965c-8.945-8.945-19.694-13.422-32.261-13.422H45.681c-12.562,0-23.313,4.477-32.264,13.422   C4.471,58.913,0,69.663,0,82.226v310.633c0,12.566,4.471,23.315,13.417,32.265c8.951,8.945,19.702,13.414,32.264,13.414h155.318   c0,7.231-1.524,14.661-4.57,22.269c-3.044,7.614-6.09,14.273-9.136,19.981c-3.042,5.715-4.565,9.897-4.565,12.56   c0,4.948,1.807,9.24,5.424,12.847c3.615,3.621,7.898,5.435,12.847,5.435h146.179c4.949,0,9.233-1.813,12.848-5.435   c3.62-3.606,5.427-7.898,5.427-12.847c0-2.468-1.526-6.611-4.571-12.415c-3.046-5.801-6.092-12.566-9.134-20.267   c-3.046-7.71-4.569-15.085-4.569-22.128h155.318c12.56,0,23.309-4.469,32.254-13.414c8.949-8.949,13.422-19.698,13.422-32.265   V82.226C548.176,69.663,543.699,58.913,534.75,49.965z M511.627,319.768c0,2.475-0.903,4.613-2.711,6.424   c-1.81,1.804-3.952,2.707-6.427,2.707H45.681c-2.473,0-4.615-0.903-6.423-2.707c-1.807-1.817-2.712-3.949-2.712-6.424V82.226   c0-2.475,0.902-4.615,2.712-6.423c1.809-1.805,3.951-2.712,6.423-2.712h456.815c2.471,0,4.617,0.904,6.42,2.712   c1.808,1.809,2.711,3.949,2.711,6.423V319.768L511.627,319.768z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#FFFFFF"/>
                </g> 
              </svg>
            </li>
          </router-link>
          <!-- Resume -->
          <router-link to="/resume">
            <li class="list-item">
              <svg version="1.1" class="nav-item" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 415 415" style="enable-background:new 0 0 415 415;" xml:space="preserve">
                <g>
                  <path d="M35,0v415h345V0H35z M365,400H50V15h315V400z"  fill="#FFFFFF"/>
                  <rect x="90" y="71" width="115" height="15" fill="#FFFFFF"/>
                  <rect x="90" y="136" width="235" height="15" fill="#FFFFFF"/>
                  <rect x="90" y="200" width="235" height="15" fill="#FFFFFF"/>
                  <rect x="90" y="264" width="235" height="15" fill="#FFFFFF"/>
                  <rect x="90" y="329" width="235" height="15" fill="#FFFFFF"/>
                </g>
              </svg>
            </li>
          </router-link>
        </ul>
      </nav>

      <router-view/>
    </div>
  </div>
</template>

<script>
import Mobile from './components/Mobile.vue'

export default {
  name: 'app',
  components: {
    Mobile,
  },
  data() {
    return {
      window: {
        width: 0,
        height: 0
      },
      location: "Norman, OK",
      phone: "(580) 786-8297",
      email: "dbrogdon91@gmail.com",
      languages: ["C/C++", "PHP", "Javascript", "HTML/CSS", "MySQL"],
      frameworks: ["Vue.js", "jQuery", "SASS", "Bootstrap"],
      tools: ["Photoshop", "Illustrator", "Visual Studio Code"],
      projects: [
        {
          title: "Melodic Odyssey",
          role: "Full Stack Developer",
          website: "https://www.melodicodyssey.com/",
          stack: "HTML/CSS, SASS, Javascript, PHP, Bootstrap",
          details: "A music education website that is built on Javascript, HTML, CSS, and SASS on the front-end. The back-end host a user registration profile built with PHP and MySQL where the user can edit different aspects of their profile. The use can upload files, change information, request a new password via email, and delete their account.",
          short: "A music education website built in JS, HTML/CSS, SASS, Bootstrap on the front end, and PHP with MySQL on the back end for the user profiles.",
          vs: "A music education website built in HTML/CSS, SASS, JS, PHP, and Bootstrap",
        },
        {
          title: "Oklahoma Botanical Identification Application",
          role: "Mobile Developer",
          website: "https://www.github.com/",
          stack: "Swift",
          details: "An iOS app developed in a pair programming environment that list the different plant species found in Oklahoma via reading a file. This was developed using Swift and xCode.",
          short: "An iOS app developed in a pair programming environment listing different plant species build with Swift",
          vs: "iOS app created in Swift to catalog different plant species",
        },
        {
          title: "Best Mold Technologies",
          role: "Database Developer",
          website: "https://www.github.com/",
          stack: "MySQL, MS Access",
          details: "Worked closely with the employees and CEO of BMT to develop software that kept track of tire molds and transactions within the company. Used Toad, MS Access, and SQL to develop a UI and a database for the software.",
          short: "Developed a database and UI for BMT that kept track of tire molds and transations with Toad, MS Access, and MySQL.",
          vs: "Database created for BMI in Toad, MS Access, and MySQL",
        },
        {
          title: "Candy Cane Shooter",
          role: "Developer",
          website: "https://www.github.com/approximatelyinfinity",
          stack: "C#, Unity",
          details: "A first person shooter created in Unity using C# with the ability to play multiplayer LAN matches."
        },
      ],
      workexp: [
        {
          company: "SDB Consulting",
          title: "IT Assistant",
          location: "Duncan, OK",
          from: "June 2014",
          to: "Aug 2018",
          details: "Helped maintain computer hardware within the company. Fixed all technical issues that arose on the company laptops. Setup new laptops for use within the company.",
          short: "Helped maintain computer hardware within the company and fixed all technical issues that arose."
        },
        {
          company: "M&M Supply Co.",
          title: "IT Assistant",
          location: "Duncan, OK",
          from: "June 2013",
          to: "Jan 2014",
          details: "Maintained computer hardware/software for thirteen stores spread across Oklahoma and Texas. Restored old hardware to working condition. Setup new workstations for the various locations. Handled technical issues over the phone with the several different stores.",
          short: "Maintained computer hardware/software for thirteen stores spread across Oklahoma and Texas."
        },
        {
          subject: "Department of Defense, U.S. Army Fires Division",
          title: "Front-End Developer",
          from: "Jan 2017",
          to: "May 2017",
          location: "Lawton, OK",
          details: "Used HTML/CSS to develop the front end for a repository for the Department of Defense. Worked very closely with the graphic design team to create their layout. Worked with the rest of the team to create the documentation for the entire project. ",
          short: "Worked with designers creating the front end for a respostory for hte Dept. of Defense."
        },
      ],
      education: [
        {
          university: "Cameron University",
          degree: "Bachelor of Science",
          subject: "Computer Science",
          location: "Lawton, OK",
          date: "Dec 2017",
        },
        {
          university: "Cameron University",
          degree: "Associates of Science",
          subject: "Information Technology",
          location: "Lawton, OK",
          date: "May 2017",
        }
      ],
    }
  },
  created() {
    //Gets screen size when the window size is changed
    window.addEventListener('resize', this.handleResize)
    this.handleResize();
    this.isMobile();
  },
  destroyed() {
    //Removes event listening, so it can be captured again
    window.removeEventListener('resize', this.handleResize)
  },
  methods: {
    burger() {
      document.getElementById("btn-menu").classList.toggle("is-active");
      document.getElementById("btn-menu").classList.toggle("btn-active");
      document.getElementById("menu").classList.toggle("menu-active");
    },
    isMobile() {
      //Detects if the device is running on a mobile browser
      if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
        return true
      } else {
        return false
      }
    },
    handleResize() {
      //Gets the windows dimensions to be set to the created() and destroyed() functions
      this.window.width = window.innerWidth;
      this.window.height = window.innerHeight;
    },
  }
}
</script>

<style lang="scss">
  @import '../src/style/burger.scss';
  @import '../src/style/globals.scss';
  @import '../src/style/buttons.scss';
  @import '../src/style/fonts.scss';

  .burger-icon {
    @include burger(32px, 3px, 6px, black, .3s);
    margin-left: auto;
    margin-right: auto;
  }
  .btn-menu.is-active .burger-icon {
    @include burger-cross;
  }

  .menu {
    z-index: 1;
    background-color: rgba(0,0,0,0.75);
    width: 128px;
    margin-top: 0px;
    position: absolute;
    display: none;
    right: 0;
  }
  .menu-active {
    display: block;
  }
  .list-item {
    height: 40px;
  }
  .nav-item {
    margin-top: 4%;
    margin-left: 40%;
    height: 24px;
    width: 24px;
  }

  html, body {
    position: relative;
    height: 100%;
    background: white;
    overflow-x: hidden;
    font-family: 'IBM Plex Sans', sans-serif;
    font-weight: 100;
    font-style: normal;
  }

  @media only screen and (max-width: 787px) {
  html, body {
    background-color: black;
  }
}
</style>
