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
                <div @click="isVisible = true" class="hero-color-item">
                    <div v-if="isVisible" class="hero-color-item-click" />
                </div>
                <div @click="isVisible = true" class="hero-color-item">
                    <div v-if="isVisible" class="hero-color-item-click" />
                </div>
                <div @click="isVisible = true" class="hero-color-item">
                    <div v-if="isVisible" class="hero-color-item-click" />
                </div>
            </div>
            <div class="hero-color-row">
                <div @click="isVisible = true" class="hero-color-item">
                    <div v-if="isVisible" class="hero-color-item-click" />
                </div>
                <div @click="isVisible = true" class="hero-color-item">
                    <div v-if="isVisible" class="hero-color-item-click" />
                </div>
                <div @click="isVisible = true" class="hero-color-item">
                    <div v-if="isVisible" class="hero-color-item-click" />
                </div>
            </div>
            <div class="hero-color-row">
                <div @click="isVisible = true" class="hero-color-item">
                    <div v-if="isVisible" class="hero-color-item-click" />
                </div>
                <div @click="isVisible = true" class="hero-color-item">
                    <div v-if="isVisible" class="hero-color-item-click" />
                </div>
                <div @click="isVisible = true" class="hero-color-item">
                    <div v-if="isVisible" class="hero-color-item-click" />
                </div>
            </div>
        </div>
        <!-- <div class="color-customization-contaiter"></div> -->
    </div>
</template>

<script>
export default {
    data() {
        return {
            pause: "Пауза",
            pauseMenuVisibility: false, // поставить true для тоггла
            customizationMenuVisibility: true,
            isVisible: false,

        }
    },
    methods: {
        hideMenu() {
            this.pauseMenuVisibility = false;
            this.customizationMenuVisibility = true;
            // или можно тоггл
            // this.inputVisibility = !this.inputVisibility;
        }

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
.pauseMenu-wrapper {
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
.hero-customization-contaiter {
    /* border: 1vh solid #000; */
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
    /* background-color: rgb(40,40,40); */
    margin: 0.1vh;
	border: 0.1vh solid #000;
}
.hero-color-item-click {
    height: 100%;
    width: 100%;
    border: 0.1vh solid #000;
}
</style>