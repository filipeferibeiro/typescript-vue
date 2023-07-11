<template>
	<div id="app">
		<ContadorComponent :valorInicial="10" />
		<ContadorClasse :valorInicial="100" />
	</div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import ContadorComponent from "@/components/ContadorComponent.vue";
import ContadorClasse from "./components/ContadorClasse.vue";

@Component({
	components: {
		ContadorComponent,
		ContadorClasse,
	},
})
export default class App extends Vue {}
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
