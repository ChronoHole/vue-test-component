<template>
	<div class="container">
		<slot name="icon"></slot>
		<h1 class="title">
			<slot name="title"></slot>
		</h1>
		<button v-on:click="action" class="button-action">Label mob</button>
	</div>
</template>

<script setup>
function action() {
	console.log('click')
}
</script>

<style scoped>
.container {
	width: auto;
	display: flex;
	align-items: center;
	justify-content: space-between;
	padding: 8px;
	background: rgb(232, 31, 47);
	background: linear-gradient(
		90deg,
		rgba(232, 31, 47, 1) 0%,
		rgba(255, 137, 131, 1) 100%
	);
	border-radius: 20px;
}

@media only screen and (max-width: 475px) {
	.container {
		width: max-content;
		margin-left: auto;
		margin-right: auto;
	}
}

.container button:last-child {
	margin-left: auto;
}

.title {
	margin: 0 14px;
	color: white;
	font-size: 20px;
	line-height: 24px;
	font-weight: 700;
}

.button-action {
	cursor: pointer;
	width: 100px;
	height: 36px;
	background: #ffffff;
	border-radius: 12px;
	border: none;
	padding: 8px 16px;
	color: #e81f2f;
	font-weight: 500;
	font-size: 14px;
	line-height: 20px;
	letter-spacing: 0.0025em;
	transition: 0.3s;
}

.button-action:hover {
	opacity: 0.9;
	box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.2);
}
</style>
