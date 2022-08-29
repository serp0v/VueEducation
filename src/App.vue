<template>
    <div v-if="pauseMenuVisibility" class="pauseMenu-wrapper">
        <div class="pauseMenu-container">
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
            <div class="hero-color-row">
                <div @click="isVisible[0] = true" class="hero-color-item">
                    <div v-if="isVisible[0]" class="hero-color-item-click" />
                </div>
                <div @click="isVisible[1] = true" class="hero-color-item">
                    <div v-if="isVisible[1]" class="hero-color-item-click" />
                </div>
                <div @click="isVisible[2] = true" class="hero-color-item">
                    <div v-if="isVisible[2]" class="hero-color-item-click" />
                </div>
            </div>
            <div class="hero-color-row">
                <div @click="isVisible[3] = true" class="hero-color-item">
                    <div v-if="isVisible[3]" class="hero-color-item-click" />
                </div>
                <div @click="isVisible[4] = true" class="hero-color-item">
                    <div v-if="isVisible[4]" class="hero-color-item-click" />
                </div>
                <div @click="isVisible[5] = true" class="hero-color-item">
                    <div v-if="isVisible[5]" class="hero-color-item-click" />
                </div>
            </div>
            <div class="hero-color-row">
                <div @click="isVisible[6] = true" class="hero-color-item">
                    <div v-if="isVisible[6]" class="hero-color-item-click" />
                </div>
                <div @click="isVisible[7] = true" class="hero-color-item">
                    <div v-if="isVisible[7]" class="hero-color-item-click" />
                </div>
                <div @click="isVisible[8] = true" class="hero-color-item">
                    <div v-if="isVisible[8]" class="hero-color-item-click" />
                </div>
            </div>
        </div>
        <!-- <div class="color-customization-contaiter"></div> -->
    </div>
</template>

<script>
    // isVisible.fill(false)
    // console.log(isVisible[3])
    // isVisible[0] = true;
export default {
    data(isVisible) {
        return {
            pause: "Пауза",
            pauseMenuVisibility: false, // поставить true для тоггла
            customizationMenuVisibility: true,
            isVisible: [false, false, false, false, false, false, false, false, false],
            
        }
    },
    methods: {
        hideMenu() {
            this.pauseMenuVisibility = false;
            this.customizationMenuVisibility = true;
            // или можно тоггл
            // this.inputVisibility = !this.inputVisibility;
        },
    }   
}
</script>

<style>
body {
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
	justify-content: center;
	align-items: center;
	position: absolute;
	z-index:9998;
	font-size: 200px;
	font-family: 'Pompiere', cursive;
	font-weight: 200;
}
/* .pauseMenu-wrapper {} */
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
.hero-customization-contaiter {
    display: flex;
    flex-direction: column;
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
</style>