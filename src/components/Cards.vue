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
						imgUrl: 'https://static.netnaija.com/i/AqgKGRo1Nr1.jpg',
						movieName: 'Space Jam: A New Legacy (2021)',
						buttonColor: 'btn-primary',
						desc:
							"Welcome to the Jam! When LeBron and his young son Dom are trapped in a digital space by a rogue A.I., LeBron must get them home safe by leading Bugs, Lola Bunny and the whole gang of notoriously undisciplined Looney Tunes to victory over the A.I.'s digitized champions on the court. It's Tunes versus Goons in the highest-stakes challenge of his life.",
					},
					{
						imgUrl: 'https://static.netnaija.com/i/Aq2NA3yn7zJ.jpg',
						movieName: 'Luca (2021)',
						buttonColor: 'btn-danger',
						desc:
							"This summer, you're invited to Portorosso. Two young boys experience an unforgettable Italian summer filled with gelato, pasta, and endless scooter rides. But all the fun is threatened by a deeply-held secret: they are sea monsters from another world just below the water's surface.",
					},
					{
						imgUrl: 'https://static.netnaija.com/i/yMX7y3lYN83.jpg',
						movieName: 'Fatherhood (2021)',
						buttonColor: 'btn-success',
						desc:
							'In it, together. A widowed new dad copes with doubts, fears, heartache, and dirty diapers as he sets out to raise his daughter on his own.',
					},
					{
						imgUrl: 'https://static.netnaija.com/i/m9z7oylWN2r.jpg',
						movieName: 'The Father (2021)',
						buttonColor: 'btn-primary',
						desc:
							'The story of Ba Sang - the second of the 4 noisy siblings: Giau, Sang, Phu, Quy. Ba Sang is a meddler, "too" kind, and always sacrifice for others despite they want it or not. Quan - Ba Sang\'s son is a modern young Youtuber.',
					},
					{
						imgUrl: 'https://static.netnaija.com/i/LqXNEoXJ7lE.jpg',
						movieName: 'Rollers (2021)',
						buttonColor: 'btn-warning',
						desc:
							'Rufus Paisley is an alcoholic who refuses to admit it. Everything he loves is gathered in one place: the "Rollers". He even gave up a promising career as a musician to stay there. But this historic place, once owned by his parents, is in difficulty and he is short of the means to save it. His friends urge him to move on, but can he?',
					},
					{
						imgUrl: 'https://static.netnaija.com/i/zxG7ZjxQ7q2.jpg',
						movieName: 'Pig (2021)',
						buttonColor: 'btn-dark',
						desc:
							"We don't get a lot of things to really care about. A truffle hunter who lives alone in the Oregonian wilderness must return to his past in Portland in search of his beloved foraging pig after she is kidnapped.",
					},
					{
						imgUrl: 'https://img.netnaija.com/GqLKHK.jpg',
						movieName: 'The Flash',
						buttonColor: 'btn-danger',
						desc:
							'Barry Allen wakes up 9 months after he was struck by lightning and discovers that the bolt gave him the power of super speed. With his new team and powers, Barry becomes "The Flash" and fights crime in Central City.',
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
