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
					@toggleShowModal="toggleShow"
				/>
			</div>
		</div>
		<Modal
			:showModal="showModal"
			@toggleShowModal="toggleShow"
			:movie="movie"
		/>
	</section>
</template>

<script>
	import Card from './Card.vue';
	import Modal from './Modal.vue';
	export default {
		name: 'Cards',
		components: {
			Card,
			Modal,
		},
		methods: {
			toggleShow(movieName) {
				this.showModal = !this.showModal;
				this.movie.movieName = movieName.moviename;
			},
		},
		data() {
			return {
				showModal: false,
				movie: { movieName: 'Not Stated' },
				movieData: [
					{
						imgUrl: 'https://static.netnaija.com/i/Aq2NA3yn7zJ.jpg',
						movieName: 'Luca (2021)',
						buttonColor: 'btn-danger',
					},
					{
						imgUrl: 'https://static.netnaija.com/i/yMX7y3lYN83.jpg',
						movieName: 'Fatherhood (2021)',
						buttonColor: 'btn-success',
					},
					{
						imgUrl: 'https://static.netnaija.com/i/m9z7oylWN2r.jpg',
						movieName: 'The Father (2021)',
						buttonColor: 'btn-primary',
					},
					{
						imgUrl: 'https://static.netnaija.com/i/LqXNEoXJ7lE.jpg',
						movieName: 'Rollers (2021)',
						buttonColor: 'btn-warning',
					},
					{
						imgUrl: 'https://img.netnaija.com/GqLKHK.jpg',
						movieName: 'The Flash',
						buttonColor: 'btn-danger',
					},
					{
						imgUrl: 'https://static.netnaija.com/i/deYakyoQKP3.jpg',
						movieName: 'Ridley Jones',
						buttonColor: 'btn-secondary',
					},
					{
						imgUrl: 'https://img.netnaija.com/3GLKHK.jpg',
						movieName: 'All American',
						buttonColor: 'btn-info',
					},
					{
						imgUrl: 'https://static.netnaija.com/i/ZOoanM3q7jA.jpg',
						movieName: 'The Chi',
						buttonColor: 'btn-secondary',
					},
					{
						imgUrl: 'https://static.netnaija.com/i/bvWaqJ3ZNrk.jpg',
						movieName: 'Dynasty',
						buttonColor: 'btn-dark',
					},
				],
			};
		},
	};
</script>

<style></style>
