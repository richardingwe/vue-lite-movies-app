<template>
	<div class="modalDiv" v-if="showModal">
		<div class="modalContainer">
			<div class="header">
				<h3 class="Title">
					Hello There
				</h3>
				<i class="fas fa-times" @click="$emit('toggleShowModal')"></i>
			</div>
			<hr />
			<div class="Body">
				Watch your assets.
				<br />
				The reboot follows two of America's wealthiest families, the Carringtons
				and the Colbys, as they feud for control over their fortune and their
				children focusing on Fallon Carrington, the daughter of billionaire
				Blake Carrington, and her soon-to-be stepmother, Cristal, a Hispanic
				woman marrying into this WASP family and America's most powerful class.
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		props: ['showModal'],
	};
</script>

<style>
	.modalDiv {
		background: rgba(128, 128, 128, 0.514);
		height: 100vh;
		width: 100vw;
		position: fixed;
		top: 0;
		z-index: 99;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.header {
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.modalContainer {
		width: 80vw;
		height: 60vh;
		background-color: rgb(245, 248, 250);
		border-radius: 5px;
		border: 1px solid black;
		padding: 5rem 4rem;
	}

	i {
		cursor: pointer;
		font-size: 2rem;
	}

	.Title,
	.Body {
		text-align: left;
		margin-bottom: 1rem;
	}
</style>
