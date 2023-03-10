<template>
	<Header />
	<Preview />
	<Menu />
	<Events/>
	<AboutUs/>
	<Footer />
</template>

<script>
	import Header from './components/Header.vue';
	import Preview from './components/Preview.vue';
	import Menu from './components/Menu.vue';
	import Events from './components/Events.vue';
	import AboutUs from './components/AboutUs.vue';
	import Footer from './components/Footer.vue';

	export default{
		components: {
			Header,
			Preview,
			Menu,
			Events,
			AboutUs,
			Footer,
		},

		data(){
			return{}
		},
	}
</script>

<style lang="scss">
	@import 'assets/main.scss';
</style>