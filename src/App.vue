<script>
import appHeader from "./components/appHeader.vue"

import axios from 'axios'; //importo Axios
import { store } from "./store.js" //state management

export default {
	components: {
		appHeader
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
		doThings() {
			console.log("App.vue does things");
		}
	}
}
</script>

<template>
	<appHeader />
	<main>

	</main>
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