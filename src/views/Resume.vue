<template>
    <div class="resume">
        <div class="container-fluid">
            <div class="row no-gutter">
                <div class="col">
                    <h1 class="font-medium title-text">Resume</h1>
                </div>
            </div>
            <div class="row no-gutter">
                <div class="col">
                    <div class="resume-title" align="right">
                        <h2>Don Brogdon</h2>
                        <h3>{{email}}</h3>
                        <h4>{{location}} --- {{phone}}</h4>
                        <router-link class="pdf-link" to="/rec">
                            <button class="resume-btn" type="button">Letters of Rec</button>
                            <span class="resume-background-btn-left2"></span>
                            <span class="resume-background-btn-bottom2"></span>
                        </router-link>
                        <span style="margin-left: 10px"></span>
                        <a class="pdf-link" href="http://www.donbrogdon.com/assets/CV.pdf" target="_blank">
                            <button class="resume-btn" type="button">View PDF</button>
                            <span class="resume-background-btn-left"></span>
                            <span class="resume-background-btn-bottom"></span>
                        </a>
                    </div>
                </div>
            </div>
            <hr/>
            <div class="row no-gutter">
                <div class="col">
                    <div class="resume-education">
                        <h4>Education</h4>
                        <h5>{{education[0].university}}</h5>
                        <p>{{education[0].degree}} in {{education[0].subject}}</p>
                        <p>{{education[1].degree}} in {{education[1].subject}}</p>
                    </div>
                </div>
                <div class="col" align="right" style="margin-top: 40px">
                    <br>
                    <p><i>{{education[0].date}}</i></p>
                    <p><i>{{education[1].date}}</i></p>
                </div>
            </div>
            <hr/>
            <div class="row no-gutter">
                <div class="col">
                    <div class="resume-projects">
                        <h4>Projects</h4>
                        <h5>{{projects[0].subject}}</h5>
                        <p><i>{{projects[0].role}}</i></p>
                        <p>{{projects[0].details}}</p>
                        <br>
                        <h5>{{projects[1].subject}}</h5>
                        <p><i>{{projects[1].role}}</i></p>
                        <p>{{projects[1].details}}</p>
                        <br>
                        <h5>{{projects[2].subject}}</h5>
                        <p><i>{{projects[2].role}}</i></p>
                        <p>{{projects[2].details}}</p>
                    </div>
                </div>
                <div class="col">
                    <div class="resume-experience">
                        <h4>Experience</h4>
                        <h5>{{workexp[0].company}}</h5>
                        <p><i>{{workexp[0].title}}</i></p>
                        <p>{{workexp[0].from}} - {{workexp[0].to}}</p>
                        <p>{{workexp[0].details}}</p>
                        <br>
                        <h5>{{workexp[1].company}}</h5>
                        <p><i>{{workexp[1].title}}</i></p>
                        <p>{{workexp[1].from}} - {{workexp[1].to}}</p>
                        <p>{{workexp[1].details}}</p>
                        <br>
                        <h5>{{workexp[2].company}}</h5>
                        <p><i>{{workexp[2].title}}</i></p>
                        <p>{{workexp[2].from}} - {{workexp[2].to}}</p>
                        <p>{{workexp[2].details}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "resume",
    data() {
        return {
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
                website: "https://www.melodicdoyssey.com/",
                stack: ["HTML", "CSS", "Javascript", "PHP", "Bootstrap"],
                details: "A music education website that is built on Javascript, HTML, CSS, and SASS on the front-end. The back-end host a user registration profile built with PHP and MySQL where the user can edit different aspects of their profile. The use can upload files, change information, request a new password via email, and delete their account."
                },
                {
                title: "Oklahoma Botanical Identification Application",
                role: "Mobile Developer",
                website: "https://www.github.com/",
                stack: ["Swift"],
                details: "An iOS app developed in a pair programming environment that list the different plant species found in Oklahoma via reading a file. This was developed using Swift and xCode.",
                },
                {
                title: "Best Mold Technologies",
                role: "Database Developer",
                website: "https://www.github.com/",
                stack: ["MySQL, MS Access"],
                details: "Worked closely with the employees and CEO of BMT to develop software that kept track of tire molds and transactions within the company. Used Toad, MS Access, and SQL to develop a UI and a database for the software.",
                },
            ],
            workexp: [
                {
                company: "SDB Consulting",
                title: "IT Assistant",
                location: "Duncan, OK",
                from: "June 2014",
                to: "Aug 2018",
                details: "Helped maintain computer hardware within the company. Fixed all technical issues that arose on the company laptops. Setup new laptops for use within the company."
                },
                {
                company: "M&M Supply Co.",
                title: "IT Assistant",
                location: "Duncan, OK",
                from: "June 2013",
                to: "Jan 2014",
                details: "Maintained computer hardware/software for thirteen stores spread across Oklahoma and Texas. Restored old hardware to working condition. Setup new workstations for the various locations. Handled technical issues over the phone with the several different stores."
                },
                {
                company: "Department of Defense, U.S. Army Fires Division",
                title: "Front-End Developer",
                from: "Jan 2017",
                to: "May 2017",
                location: "Lawton, OK",
                details: "Used HTML/CSS to develop the front end for a repository for the Department of Defense. Worked very closely with the graphic design team to create their layout. Worked with the rest of the team to create the documentation for the entire project. ",
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
    }
}
</script>

<style scoped lang="scss">
@import './src/style/globals.scss';
@import './src/style/fonts.scss';
@import './src/style/buttons.scss';

.title-text {
    margin-left: 24px;
    border-bottom: 1px solid black;
    margin-right: 24px;
}
p {
    margin-top: -5px;
    margin-bottom: 4px;
}
.resume-btn {
    position: relative;
}
.pdf-link:hover {
    span {
        display: inline-block;
    }
}
.resume-background-btn-left {
    position: absolute;
    margin-top: 1.5px;
    margin-left: -87px;
    display: none;
}
.resume-background-btn-bottom {
    position: absolute;
    margin-top: 39px;
    margin-left: -86px;
    display: none;
}
.resume-background-btn-left2 {
    position: absolute;
    margin-top: 2px;
    margin-left: -116px;
    display: none;
}
.resume-background-btn-bottom2 {
    position: absolute;
    margin-top: 41px;
    margin-left: -114px;
    display: none;
}
</style>