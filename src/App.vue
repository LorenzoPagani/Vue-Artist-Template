<script>
import appHeader from "./components/appHeader.vue"
import classFeatures from "./components/classFeatures.vue"
import appVideo from "./components/appVideo.vue"
import courseCatalogue from "./components/courseCatalogue.vue"
import testimonials from "./components/testimonials.vue"
import appBlog from "./components/appBlog.vue"
import events from "./components/events.vue"
import newsletterForm from "./components/newsletterForm.vue"
import appFooter from "./components/appFooter.vue"


import axios from 'axios'; //importo Axios
import { store } from "./store.js" //state management

export default {
	components: {
		appHeader,
		classFeatures,
		appVideo,
		courseCatalogue,
		testimonials,
		appBlog,
		events,
		newsletterForm,
		appFooter

	},
	data() {
		return {
			store
		}
	},
	mounted() {


		// axios.get("indirizzo").then(risultato => {
		// 	console.log(risultato);
		// }).catch(errore => {
		// 	console.error(errore);
		// });
	},
	methods: {
		updateCoordinates(event) {
			store.mouseX = event.clientX / 300;
			store.mouseY = event.clientY / 70;
		},
	}
}
</script>

<template>
	<div class="wrapper overflow-x-hidden" @mousemove="updateCoordinates">
		<appHeader />
		<main>
			<classFeatures />
			<appVideo />
			<testimonials />
			<courseCatalogue />
			<appBlog />
			<events />
		</main>
		<footer>
			<newsletterForm />
			<appFooter />
		</footer>
	</div>
</template>

<style lang="scss">
// importo il foglio di stile generale dell'applicazione, non-scoped
@use './styles/general.scss';
</style>

<style scoped lang="scss">
@use './styles/partials/variables' as *;
</style>