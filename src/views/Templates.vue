<template>
    <div class="template">
        <div class="container-fluid">
            <div class="row no-gutter">
                <div class="col">
                    <h1 class="font-medium title-text">Templates</h1>
                </div>
            </div>
            <div class="row no-gutter">
                <div class="col">
                    <div class="background-img">
                        <div class="template-background">
                            <h2 class="font-medium template-title">Dog Grooming</h2>
                            <p class="template-stack">Front-End: HTML/CSS, JS, Vue.js, Bootstrap</p>
                            <a href="http://www.donbrogdon.com/templates/dog/index.html">
                                <button class="btn-outline-dark template-visit-btn" type="button">Visit</button> 
                                <span class="template-background-btn-left"></span>
                                <span class="template-background-btn-bottom"></span>
                            </a>
                            <span class="template-background-left"></span>
                            <span class="template-background-bottom"></span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "template",
    data() {
        return {

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

.template-background {
    height: 320px;
    width: 320px;
    background-image: url('../assets/dog.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    position: absolute;
}
.template-background:hover {
    margin-left: 10px;
    margin-top: -5px;
    background: rgb(236,107,143);
    background: -moz-linear-gradient(60deg, rgba(236,107,143,1) 25%, rgba(148,186,38,1) 75%);
    background: -webkit-linear-gradient(60deg, rgba(236,107,143,1) 25%, rgba(148,186,38,1) 75%);
    background: linear-gradient(60deg, rgba(236,107,143,1) 25%, rgba(148,186,38,1) 75%);
    filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#ec6b8f",endColorstr="#94ba26",GradientType=1);

    .template-title {
        display: block;
    }
    .template-stack {
        display: block;
    }
    .template-visit-btn {
        display: block;
    }
}

.template-title {
    color: white;
    border-bottom: 1px solid white;
    margin-left: 10px;
    display: none;
}
.template-background-left {
    width: 10px;
    height: 320px;
    background-color: map-get($colors, primary-dark);
    position: absolute;
    transform: skewY(-40deg);
    margin-top: -43px;
    margin-left: -10px;
    display: none;
}
.template-background-bottom {
    width: 320px;
    height: 10px;
    background-color: map-get($colors, primary-dark);
    position: absolute;
    margin-top: 272px;
    margin-left: -5.5px;
    transform: skewX(-49deg);
    display: none;
}

.template-stack {
    color: white;
    position: absolute;
    margin-left: 10px;
    display: none;
}

.template-visit-btn {
    margin-left: 16px;
    margin-top: 185px;
    position: absolute;
    display: none;
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
</style>