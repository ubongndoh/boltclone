<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import NavBar from './components/NavBar.vue';
import Footer from './components/Footer.vue';
import Main from './components/Main.vue';
//import HelloWorld from './components/HelloWorld.vue';
</script>

<template>
	<div>
		<NavBar />

		<Main />
		<Footer />
	</div>
</template>

<style>
body {
	background: black;
}
#app {
	font-family: BoltHelvNu, Helvetica Neue, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}
</style>
