<template>
	<div id="app">
		<ProfileSignUp></ProfileSignUp>
	</div>
</template>

<script>
import ProfileSignUp from "./components/ProfileSignUp.vue";

export default {
	name: "App",
	components: {
		ProfileSignUp,
	},
};
</script>

<style>
#app {
	padding: 10px;
	display: flex;
	justify-content: center;
	align-items: center;
}

body {
	display: flex;
	justify-content: center;
	align-items: center;
	height: 100vh;
	background-color: #eeeff3 !important;
}

@media (max-width: 576px) {
	body {
		height: auto;
	}
}

@font-face {
	font-family: "KyivType";
	src: url("assets/fonts/KyivType\ Sans\ Regular.otf") format("truetype");
	font-weight: normal;
}

@font-face {
	font-family: "Jost";
	src: url("assets/fonts/Jost-Regular.ttf") format("truetype");
	font-weight: 400;
}

@font-face {
	font-family: "Jost";
	src: url("assets/fonts/Jost-Medium.ttf") format("truetype");
	font-weight: 500;
}

@font-face {
	font-family: "TT Norms";
	src: url("assets/fonts/TTNorms-Regular.otf") format("truetype");
}
</style>
