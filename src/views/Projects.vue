<template>
    <div class="projects">
        <div class="container-fluid">
            <div class="row no-gutter">
                <div class="col">
                    <h1 class="font-medium title-text">Projects</h1>
                </div>
            </div>
            <div class="row no-gutter">
                <div class="col">
                    <div class="background-img">
                        <div class="project-background-img-mo">
                            <h2 class="font-medium project-title">Melodic Odyssey</h2>
                            <p class="font-medium project-stack">{{projects[0].stack}}</p>
                            <p class="font-small project-details">{{projects[0].details}}</p>
                            <a :href="projects[0].website">
                                <button class="btn-outline-dark project-visit-btn" type="button">Visit</button>
                                <span class="background-btn-left"></span>
                                <span class="background-btn-bottom"></span>
                            </a>
                            <span class="project-background-left"></span>
                            <span class="project-background-bottom"></span>
                        </div>
                    </div>
                </div>
                 <div class="col">
                    <div class="background-img">
                        <div class="project-background-img-cc">
                            <h2 class="font-medium project-title">Candy Cane Shooter</h2>
                            <p class="font-medium project-stack">{{projects[1].stack}}</p>
                            <p class="font-small project-details">{{projects[1].details}}</p>
                            <a :href="projects[1].website">
                                <button class="btn-outline-dark project-visit-btn-cc" type="button">Visit</button>
                                <span class="background-btn-left-cc"></span>
                                <span class="background-btn-bottom-cc"></span>
                            </a>
                            <span class="project-background-left"></span>
                            <span class="project-background-bottom"></span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "projects",
    data() {
        return {
            projects: [
                {
                title: "Melodic Odyssey",
                role: "Full Stack Developer",
                website: "https://www.melodicodyssey.com/",
                stack: "HTML/CSS, SASS, Javascript, PHP, Bootstrap",
                details: "A music education website that is built on Javascript, HTML, CSS, and SASS on the front-end. The back-end host a user registration profile built with PHP and MySQL where the user can edit different aspects of their profile. The user can upload files, change information, request a new password via email, and delete their account."
                },
                {
                title: "Candy Cane Shooter",
                role: "Developer",
                website: "https://github.com/ApproximatelyInfinity/Candy-Cane-Shooter",
                stack: "C#, Unity",
                details: "A first person shooter created in Unity using C# with the ability to play multiplayer LAN matches."
                },
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
    margin-left: 10px;
    font-weight: 200;
    border-bottom: 1px solid black;
    margin-right: 10px;
}

.background-img {
    position: relative;
    margin-top: 150px;
}
.background-img:hover {
    span {
        display: inline-block;
    }
}
.project-background-img-mo {
    height: 320px;
    width: 320px;
    background-image: url('../assets/melodicodyssey.png');
    background-repeat: no-repeat;
    background-size: cover;
    position: absolute;
    margin-top: 5px;
    
}
.project-background-img-mo:hover {
    margin-left: 10px;
    margin-top: -5px;
    background: rgb(82,7,170);
    background: -moz-linear-gradient(220deg, rgba(82,7,170,1) 0%, rgba(110,30,203,1) 25%, rgba(227,182,94,1) 100%);
    background: -webkit-linear-gradient(220deg, rgba(82,7,170,1) 0%, rgba(110,30,203,1) 25%, rgba(227,182,94,1) 100%);
    background: linear-gradient(220deg, rgba(82,7,170,1) 0%, rgba(110,30,203,1) 25%, rgba(227,182,94,1) 100%);
    filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#5207aa",endColorstr="#e3b65e",GradientType=1);

    .project-title {
        display: inline-block;
    }
    .project-visit {
        display: inline-block;
    }
    .project-stack {
        display: inline-block;
    }
    .project-details {
        display: inline-block;
    }
    .project-visit-btn {
        display: inline-block;
    }
}

.project-background-left {
    width: 10px;
    height: 320px;
    background-color: map-get($colors, primary);
    position: absolute;
    transform: skewY(-40deg);
    display: none;
    margin-top: 4px;
    margin-left: -68px;
}
.project-background-bottom {
    width: 322px;
    height: 10px;
    background-color: map-get($colors, primary);
    position: absolute;
    margin-top: 319px;
    margin-left: -64px;
    transform: skewX(-42deg);
    display: none;
}


.project-title {
    margin-left: 12px;
    margin-top: 10px;
    position: absolute;
    color: white;
    border-bottom: 1px solid white;
    display: none;
}

.project-stack {
    margin-top: 48px;
    margin-left: 12px;
    position: absolute;
    color: white;
    display: none;
    font-size: 14px;
    transform: skew(-16deg);
}
.project-details {
    margin-top: 82px;
    margin-left: 12px;
    position: absolute;
    color: white;
    display: none;
    font-size: 14px;
}
.project-visit-btn {
    margin-top: 240px;
    margin-left: 12px;
    display: none;
}
.background-btn-left {
    position: absolute;
    margin-top: 242px;
    margin-left: -50px;
    display: none;
    
}
.background-btn-bottom {
    position: absolute;
    margin-top: 279px;
    margin-left: -48px;
    display: none;
}

.project-visit-btn:hover {
    .background-btn-left {
        display: inline-block;
    }
    .background-btn-bottom {
        display: inline-block;
    }
}

.project-background-img-cc {
    height: 320px;
    width: 320px;
    background-image: url('../assets/cc.png');
    background-repeat: no-repeat;
    background-size: cover;
    position: absolute;
    margin-top: 5px;
    
}
.project-background-img-cc:hover {
    margin-left: 10px;
    margin-top: -5px;
    background: rgb(16,130,21);
    background: -moz-linear-gradient(229deg, rgba(16,130,21,1) 0%, rgba(108,113,0,1) 50%, rgba(251,5,5,1) 100%);
    background: -webkit-linear-gradient(229deg, rgba(16,130,21,1) 0%, rgba(108,113,0,1) 50%, rgba(251,5,5,1) 100%);
    background: linear-gradient(229deg, rgba(16,130,21,1) 0%, rgba(108,113,0,1) 50%, rgba(251,5,5,1) 100%);
    filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#108215",endColorstr="#fb0505",GradientType=1);

    .project-title {
        display: inline-block;
    }
    .project-visit {
        display: inline-block;
    }
    .project-stack {
        display: inline-block;
    }
    .project-details {
        display: inline-block;
    }
    .project-visit-btn-cc {
        display: inline-block;
    }
}

.project-visit-btn-cc {
    margin-top: 240px;
    margin-left: 12px;
    display: none;
}
.background-btn-left-cc {
    position: absolute;
    margin-top: 242px;
    margin-left: -50px;
    display: none;
    
}
.background-btn-bottom-cc {
    position: absolute;
    margin-top: 279px;
    margin-left: -48px;
    display: none;
}

.project-visit-btn-cc:hover {
    .background-btn-left-cc {
        display: inline-block;
    }
    .background-btn-bottom-cc {
        display: inline-block;
    }
}
</style>