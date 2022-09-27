<template>
<!-- v-if="pauseMenuVisibility" -->
    <div class="pauseMenu-wrapper">
        <button @click="count++">
        Count is: {{ count }}
        </button>
        <!-- <div class="pauseMenu-container">
            <div class="pause-title">{{ pause }}</div>
            <div class="pause-menu-buttons">
                <div @click="hideMenu" class="pause-menu-button">Вернуться в игру</div>
            </div>
            <div class="pause-menu-buttons">
                <div @click="hideMenu" class="pause-menu-button">Кастомизация</div>
            </div>
            <div class="pause-menu-buttons">
                <div @click="hideMenu" class="pause-menu-button">В главное меню</div>
            </div>
        </div>
    </div>
    <div v-if="customizationMenuVisibility" class="customizationMenu-wrapper">
        <div class="hero-customization-contaiter">
            <div class="hero-customization-body">
                <div class="hero-color-row">
                    <div @click="isVisible[0] = !isVisible[0]" class="hero-color-item">
                        <div v-if="isVisible[0]" class="hero-color-item-click" />
                    </div>
                    <div @click="isVisible[1] = !isVisible[1]" class="hero-color-item">
                        <div v-if="isVisible[1]" class="hero-color-item-click" />
                    </div>
                    <div @click="isVisible[2] = !isVisible[2]" class="hero-color-item">
                        <div v-if="isVisible[2]" class="hero-color-item-click" />
                    </div>
                </div>
                <div class="hero-color-row">
                    <div @click="isVisible[3] = !isVisible[3]" class="hero-color-item">
                        <div v-if="isVisible[3]" class="hero-color-item-click" />
                    </div>
                    <div @click="isVisible[4] = !isVisible[4]" class="hero-color-item">
                        <div v-if="isVisible[4]" class="hero-color-item-click" />
                    </div>
                    <div @click="isVisible[5] = !isVisible[5]" class="hero-color-item">
                        <div v-if="isVisible[5]" class="hero-color-item-click" />
                    </div>
                </div>
                <div class="hero-color-row">
                    <div @click="isVisible[6] = !isVisible[6]" class="hero-color-item">
                        <div v-if="isVisible[6]" class="hero-color-item-click" />
                    </div>
                    <div @click="isVisible[7] = !isVisible[7]" class="hero-color-item">
                        <div v-if="isVisible[7]" class="hero-color-item-click" />
                    </div>
                    <div @click="isVisible[8] = !isVisible[8]" class="hero-color-item">
                        <div v-if="isVisible[8]" class="hero-color-item-click" />
                    </div>
                </div>
            </div>
        </div>
        <div class="color-customization-contaiter">
            <div class="color-customization-bar">
                <div class="color-select-row color-top-row">
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                </div>
                <div class="color-select-row">
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                    <div class="color-select-item"></div>
                </div>
            </div>
        </div> -->
    </div>
</template>

<script>
    // isVisible.fill(false)
    // console.log(isVisible[3])
    // isVisible[0] = true;
export default {
    data() {
        return {
            // pause: "Пауза",
            // pauseMenuVisibility: false, // поставить true для тоггла
            // customizationMenuVisibility: true,
            // isVisible: [false, false, false, false, false, false, false, false, false],
            count: 0,
        }
    },
    // methods: {
    //     hideMenu() {
    //         this.pauseMenuVisibility = false;
    //         this.customizationMenuVisibility = true;
    //     },
    // }   
}
</script>

<style>
body,html {
    height: 100vh;
    width: 100vw;
    overflow: hidden;
    margin: 0;
    padding: 0;
    user-select:none;
}
[class$="-wrapper"] {
    width: 100vw;
	height: 100vh;
	display: flex;
	position: absolute;
	z-index:9998;
	font-size: 200px;
	font-family: 'Pompiere', cursive;
	font-weight: 200;
}
/* .pauseMenu-wrapper {
    justify-content: center;
    align-items: center;
}
.customizationMenu-wrapper {
    flex-direction: column;
}
.pauseMenu > p {
	border: 0.1vh solid #000;
}
.pauseMenu-container {
	display: flex;
	width: 70vh;
	height: 43vh;
	border: 0.1vh solid #000;
	font-size: 3vh;
	flex-direction: column;
	background-color: #fff;
}
.pauseMenu-container > div {
	display: flex;
	flex-direction: column;
	width: 100%;
	height: 25%;
	align-items: center;
}
.pauseMenu-container > div > div {
	width: 33vh;
	height: 8vh;
	display: flex;
	border: 0.1vh solid #000;
	justify-content: center;
	align-items: center;
}
.pause-title {
	justify-content: center;
}

.color-customization-contaiter {
    display: flex;
    width: 100vw;
    height: 60vh;
}
.hero-customization-body {
    display: flex;
    justify-content: end;
	align-items: center;
    flex-direction: column;
    height: 69.5vh;
}
.hero-color-row {
    display: flex;
    flex-direction: row;
}
.hero-color-item {
    height: 13vh;
    width: 13vh;
    margin: 0.1vh;
	border: 0.1vh solid #000;
}
.hero-color-item-click {
    height: 100%;
    width: 100%;
    border: 0.1vh solid #000;
}
/*  */
/* .color-customization-contaiter {

    display: flex;
    width: 100vw;
    height: 30.5vh;
    justify-content: center;
    align-items: center;
}
.color-customization-bar {
    border: 0.1vh solid #000;
    display: flex;
    flex-direction: column;
}
.color-select-row {
    width: 100%;
    height: 50%;
    display: flex;
    flex-direction: row;
    padding-left: 1vh;
    padding-right: 1vh;
    padding-bottom: 0.5vh;
}
.color-select-item {
    width: 4vh;
    height: 4vh;
    border: 0.1vh solid #000;
}
.color-top-row {
    padding-top: 0.5vh;
}
.color-select-item ~ .color-select-item {
    margin-left: 1vh;
}  */
button {
    /* height: 30px; */
    display: flex;
    /* width: 100px; */
    /* position: absolute; */
    border: none;
    /* top: 50%; */
    /* left: 50%; */
    margin: auto auto;
    font-size: 20px;
    border-radius: 5px;
    color: aliceblue;
    padding: 5px;
    background-color: #404040;
    /* justify-self: center;
    align-items: center; */
}
</style>