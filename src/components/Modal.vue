<template>
	<div @click.self="closeModal" class="modalDiv" v-show="showModal">
		<div class="modalContainer">
			<div class="header">
				<h3 class="Title">
					{{ movie.movieName }}
				</h3>
				<i class="fas fa-times" @click="$emit('toggleShowModal')"></i>
			</div>
			<hr />
			<div class="Body">
				{{ movie.movieDesc }}
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		props: ['showModal', 'movie'],
		methods: {
			closeModal(e) {
				if (!e.target.classList.contains('modalContainer'))
					this.$emit('toggleShowModal');
			},
		},
	};
</script>

<style>
	.modalDiv {
		/* background: rgba(128, 128, 128, 0.514); */
		height: 100vh;
		width: 100vw;
		position: fixed;
		top: 0;
		z-index: 99;
		display: flex;
		align-items: center;
		justify-content: center;
		background: linear-gradient(
			-45deg,
			rgba(255, 255, 255, 0.1),
			rgba(255, 255, 255, 0.4)
		);
		box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
		backdrop-filter: blur(4px);
		-webkit-backdrop-filter: blur(4px);
		border-radius: 10px;
		border: 1px solid rgba(255, 255, 255, 0.18);
	}

	.header {
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.modalContainer {
		width: 80vw;
		background-color: rgb(245, 248, 250);
		border-radius: 5px;
		border: 1px solid black;
		padding: 5rem 4rem;
	}

	i {
		cursor: pointer;
		font-size: 1.5rem;
	}

	.Title,
	.Body {
		text-align: left;
		margin-bottom: 1rem;
	}

	@media (max-width: 480px) {
		.modalContainer {
			width: 80vw;
			background-color: rgb(245, 248, 250);
			border-radius: 5px;
			border: 1px solid black;
			padding: 2rem 2.5rem;
		}
	}
</style>
