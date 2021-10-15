<template>
	<section class="movies py-5">
		<div class="container">
			<h1 class="text-center mb-5 display-3">Movies</h1>

			<div class="row">
				<Card
					v-for="movie in movieData"
					:key="movie.movieName"
					:imgUrl="movie.imgUrl"
					:movieName="movie.movieName"
					:buttonColor="movie.buttonColor"
					:desc="movie.desc"
					@toggleShowModal="openModal"
				/>
			</div>
		</div>
		<Modal
			:showModal="showModal"
			@toggleShowModal="closeModal"
			:movie="movie"
		/>
	</section>
</template>

<script>
	import Card from './Card.vue';
	import Modal from './Modal.vue';
	export default {
		props: ['movieData'],
		name: 'Cards',
		components: {
			Card,
			Modal,
		},
		methods: {
			openModal(movieName) {
				this.showModal = !this.showModal;
				this.movie.movieName = movieName.moviename;
				this.movie.movieDesc = movieName.movieDesc;
			},
			closeModal() {
				this.showModal = !this.showModal;
			},
		},
		data() {
			return {
				showModal: false,
				movie: { movieName: 'Not Stated', movieDesc: '...' },
			};
		},
	};
</script>

<style></style>
