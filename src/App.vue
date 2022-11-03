<!--Компонент имеет две точки распространения контента, одна для иконки, вторая для заголовка-->
<template>
	<TestComponent>
		<template v-slot:icon><SVGComponent /></template>
		<template v-slot:title>Title Big Mob</template>
	</TestComponent>
</template>

<script setup>
import SVGComponent from './components/SVGComponent.vue'
import TestComponent from './components/TestComponent.vue'
</script>

<style>
* {
	font-family: 'Manrope', sans-serif;
}
</style>
