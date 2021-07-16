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
						desc:
							"When the museum comes alive, the adventures begin. Curious kid Ridley and her friends protect the Museum of Natural History's treasures and keep its magical secret safe: Everything comes alive at night!",
					},
					{
						imgUrl: 'https://img.netnaija.com/3GLKHK.jpg',
						movieName: 'All American',
						buttonColor: 'btn-info',
						desc:
							'When a rising high school football player from South Central L.A. is recruited to play for Beverly Hills High, the wins, losses and struggles of two families from vastly different worlds - Compton and Beverly Hills - begin to collide. Inspired by the life of pro football player Spencer Paysinger.',
					},
					{
						imgUrl: 'https://static.netnaija.com/i/ZOoanM3q7jA.jpg',
						movieName: 'The Chi',
						buttonColor: 'btn-secondary',
						desc:
							'Innocence lost. Redemption found. A relevant, timely, and distinctive coming-of-age story following a half dozen interrelated characters in the South Side of Chicago. The story centers on Brandon, an ambitious and confident young man who dreams about opening a restaurant of his own someday, but is conflicted between the promise of a new life and his responsibility to his mother and teenage brother back in the South Side.',
					},
					{
						imgUrl: 'https://static.netnaija.com/i/bvWaqJ3ZNrk.jpg',
						movieName: 'Dynasty',
						buttonColor: 'btn-dark',
						desc:
							"Watch your assets. The reboot follows two of America's wealthiest families, the Carringtons and the Colbys, as they feud for control over their fortune and their children focusing on Fallon Carrington, the daughter of billionaire Blake Carrington, and her soon-to-be stepmother, Cristal, a Hispanic woman marrying into this WASP family and America's most powerful class.",
					},
					{
						imgUrl: 'https://static.netnaija.com/i/gEeK89pl7P8.jpg',
						movieName: 'El Cid',
						buttonColor: 'btn-warning',
						desc:
							'El Cid retells from a contemporary perspective the story of the most famous Spaniard in history, a man trapped between two worlds and two cultures. A nobleman, a hero, a mercenary, a vassal, but also a man who could have been king. El Cid was centuries ahead of his time and became transcended by his own legend.',
					},
				],
			};
		},
	};
</script>

<style></style>
