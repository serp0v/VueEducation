<template>
    <div v-if="menuVisibility" class="pauseMenu-wrapper">
        <div class="pauseMenu-container">
            <div class="pause-title">{{ pause }}</div>
            <div class="pause-menu-buttons">
                <div @click="hideMenu" class="pause-menu-button">Вернуться в игру</div>
            </div>
            <div class="pause-menu-buttons">
                <div @click="hideMenu" class="pause-menu-button">Топ</div>
            </div>
            <div class="pause-menu-buttons">
                <div @click="hideMenu" class="pause-menu-button">В главное меню</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            pause: "Пауза",
            menuVisibility: true,
        }
    },
    methods: {
        hideMenu() {
            this.menuVisibility = false;
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
.pauseMenu-wrapper {
	width: 100%;
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
</style>