<template>
	<div>
		<h1>Contador Classe</h1>
		<h2>{{ valorInicial || 0 }}</h2>
		<h3>{{ parOuImpar }}</h3>
		<button @click="setValor(-1)">Dec</button>
		<button @click="setValor(1)">Inc</button>
	</div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from "vue-property-decorator";

@Component({})
export default class ContadorClasse extends Vue {
	@Prop(Number)
	public valorInicial?: number;
	public valor: number = this.valorInicial || 0;

	public setValor(delta: number) {
		if (this.valorInicial) {
			this.valorInicial += delta;
		} else {
			this.valorInicial = delta;
		}
	}
	// metodo
	public getParOuImpar(): string {
		if (!this.valorInicial) {
			return "Par";
		}
		return this.valorInicial % 2 === 0 ? "Par" : "Impar";
	}
	// prop computada
	public get parOuImpar(): string {
		if (!this.valorInicial) {
			return "Par";
		}
		return this.valorInicial % 2 === 0 ? "Par" : "Impar";
	}
}
</script>

<style></style>
