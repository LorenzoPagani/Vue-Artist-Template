<script>
import appHeader from "./components/appHeader.vue"
import classFeatures from "./components/classFeatures.vue"
import appVideo from "./components/appVideo.vue"
import courseCatalogue from "./components/courseCatalogue.vue"
import testimonials from "./components/testimonials.vue"
import appBlog from "./components/appBlog.vue"
import events from "./components/events.vue"
import newsletterForm from "./components/newsletterForm.vue"


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

	},
	data() {
		return {
			store
		}
	},
	mounted() {
		this.doThings();

		// axios.get("indirizzo").then(risultato => {
		// 	console.log(risultato);
		// }).catch(errore => {
		// 	console.error(errore);
		// });
	},
	methods: {

	}
}
</script>

<template>
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
	</footer>
</template>

<style lang="scss">
// importo il foglio di stile generale dell'applicazione, non-scoped
@use './styles/general.scss';
</style>

<style scoped lang="scss">
@use './styles/partials/variables' as *;



main {
	padding: 1rem;
}
</style>