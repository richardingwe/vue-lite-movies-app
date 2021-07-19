<template>
	<div @click="showForm = !showForm" class="add">
		<i class="fas fa-plus" :class="{ rotate: showForm }"></i>
	</div>

	<div v-show="showForm">
		<AddMovie @getNewMovie="getMovie" />
	</div>
	<Cards :movieData="movieData" />
	<!-- <section class="container">
		<div class="row section">
			<div class="col-lg-8 section-1">
				<div class="one my-3">
					Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque
					perferendis ut est quidem aliquam cum facere eveniet, distinctio
					possimus officiis quia maxime perspiciatis quos repellendus enim atque
					autem expedita aperiam quis veritatis! Adipisci magnam impedit
					accusamus praesentium reiciendis aut possimus repudiandae aliquid?
					Illo, aut. Iure perspiciatis blanditiis eaque quas mollitia optio
					odio, provident, reiciendis veniam nostrum vel autem voluptates
					eveniet, nam alias quod non iste cum laboriosam dignissimos fuga vero
					aperiam. Repellat, pariatur voluptates laboriosam, illum incidunt aut
					dolorem ratione atque commodi ullam molestiae reiciendis rem nesciunt
					ipsam accusamus aliquam voluptatibus quaerat. Ipsum quis, repellat
					odit saepe cupiditate sunt natus?
				</div>
				<div class="one my-3">
					Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque
					perferendis ut est quidem aliquam cum facere eveniet, distinctio
					possimus officiis quia maxime perspiciatis quos repellendus enim atque
					autem expedita aperiam quis veritatis! Adipisci magnam impedit
					accusamus praesentium reiciendis aut possimus repudiandae aliquid?
					Illo, aut. Iure perspiciatis blanditiis eaque quas mollitia optio
					odio, provident, reiciendis veniam nostrum vel autem voluptates
					eveniet, nam alias quod non iste cum laboriosam dignissimos fuga vero
					aperiam. Repellat, pariatur voluptates laboriosam, illum incidunt aut
					dolorem ratione atque commodi ullam molestiae reiciendis rem nesciunt
					ipsam accusamus aliquam voluptatibus quaerat. Ipsum quis, repellat
					odit saepe cupiditate sunt natus?
				</div>
				<div class="one my-3">
					Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque
					perferendis ut est quidem aliquam cum facere eveniet, distinctio
					possimus officiis quia maxime perspiciatis quos repellendus enim atque
					autem expedita aperiam quis veritatis! Adipisci magnam impedit
					accusamus praesentium reiciendis aut possimus repudiandae aliquid?
					Illo, aut. Iure perspiciatis blanditiis eaque quas mollitia optio
					odio, provident, reiciendis veniam nostrum vel autem voluptates
					eveniet, nam alias quod non iste cum laboriosam dignissimos fuga vero
					aperiam. Repellat, pariatur voluptates laboriosam, illum incidunt aut
					dolorem ratione atque commodi ullam molestiae reiciendis rem nesciunt
					ipsam accusamus aliquam voluptatibus quaerat. Ipsum quis, repellat
					odit saepe cupiditate sunt natus?
				</div>
			</div>
			<div class="col-lg-4 section-2">
				<div class="two mb-3">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis
					iusto cum, odio deleniti tenetur minima veniam vero reprehenderit
					voluptates natus sed asperiores assumenda corrupti, porro nemo quae
					quidem dignissimos, quasi rerum velit ipsum aut ratione atque. Autem
					quisquam eum reiciendis nostrum distinctio placeat et ex iusto
					voluptate possimus iure voluptates impedit architecto totam aspernatur
					odit commodi, magnam unde excepturi officiis. Dignissimos, laboriosam
					odit fugiat eaque aliquid necessitatibus quae culpa omnis facere
					maiores voluptatum voluptates perferendis vel voluptatem accusantium.
					Ut aliquid debitis tempora explicabo ea! Impedit, animi voluptatem
					nobis eius culpa nihil quos saepe, corporis nulla, suscipit aliquam
					quam sed doloremque accusamus! Ipsa veniam qui, quas eum asperiores
					praesentium iure, beatae debitis repellendus facere iste aspernatur
					odio enim modi voluptatem. Maiores nostrum quas corrupti fugit esse
					sed repellat magnam soluta non veniam sunt, adipisci laudantium,
					asperiores molestias velit blanditiis illo cupiditate nobis
					perferendis tenetur nesciunt quia veritatis reprehenderit error.
					Cupiditate, amet.
				</div>
				<div class="two mb-3">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis
					iusto cum, odio deleniti tenetur minima veniam vero reprehenderit
					voluptates natus sed asperiores assumenda corrupti, porro nemo quae
					quidem dignissimos, quasi rerum velit ipsum aut ratione atque. Autem
					quisquam eum reiciendis nostrum distinctio placeat et ex iusto
					voluptate possimus iure voluptates impedit architecto totam aspernatur
					odit commodi, magnam unde excepturi officiis. Dignissimos, laboriosam
					odit fugiat eaque aliquid necessitatibus quae culpa omnis facere
					maiores voluptatum voluptates perferendis vel voluptatem accusantium.
					Ut aliquid debitis tempora explicabo ea! Impedit, animi voluptatem
					nobis eius culpa nihil quos saepe, corporis nulla, suscipit aliquam
					quam sed doloremque accusamus! Ipsa veniam qui, quas eum asperiores
					praesentium iure, beatae debitis repellendus facere iste aspernatur
					odio enim modi voluptatem. Maiores nostrum quas corrupti fugit esse
					sed repellat magnam soluta non veniam sunt, adipisci laudantium,
					asperiores molestias velit blanditiis illo cupiditate nobis
					perferendis tenetur nesciunt quia veritatis reprehenderit error.
					Cupiditate, amet.
				</div>
				<div class="two mb-3">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis
					iusto cum, odio deleniti tenetur minima veniam vero reprehenderit
					voluptates natus sed asperiores assumenda corrupti, porro nemo quae
					quidem dignissimos, quasi rerum velit ipsum aut ratione atque. Autem
					quisquam eum reiciendis nostrum distinctio placeat et ex iusto
					voluptate possimus iure voluptates impedit architecto totam aspernatur
					odit commodi, magnam unde excepturi officiis. Dignissimos, laboriosam
					odit fugiat eaque aliquid necessitatibus quae culpa omnis facere
					maiores voluptatum voluptates perferendis vel voluptatem accusantium.
					Ut aliquid debitis tempora explicabo ea! Impedit, animi voluptatem
					nobis eius culpa nihil quos saepe, corporis nulla, suscipit aliquam
					quam sed doloremque accusamus! Ipsa veniam qui, quas eum asperiores
					praesentium iure, beatae debitis repellendus facere iste aspernatur
					odio enim modi voluptatem. Maiores nostrum quas corrupti fugit esse
					sed repellat magnam soluta non veniam sunt, adipisci laudantium,
					asperiores molestias velit blanditiis illo cupiditate nobis
					perferendis tenetur nesciunt quia veritatis reprehenderit error.
					Cupiditate, amet.
				</div>
			</div>
		</div>
	</section> -->
</template>

<script>
	import Cards from './components/Cards.vue';
	import AddMovie from './components/AddMovie.vue';

	export default {
		name: 'App',
		components: {
			Cards,
			AddMovie,
		},
		methods: {
			getMovie(newMovie) {
				this.movieData = [newMovie, ...this.movieData];
				console.log(this.movieData);
				this.showForm = false;
			},
		},
		data() {
			return {
				showForm: false,
				movie: {},
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

<style>
	.add {
		width: 50px;
		height: 50px;
		margin: 0 auto;
		background: black;
		display: flex;
		justify-content: center;
		align-items: center;
		border-radius: 50%;
		transition: 200ms ease;
		cursor: pointer;
	}

	.add:hover {
		transform: scale(1.3);
	}

	.add i {
		color: white;
	}

	.rotate {
		transform: rotate(45deg);
		transition: 200ms ease;
	}

	.section-1 {
		height: 1000px;
	}

	.section-2 {
		height: 1200px;
	}

	.one {
		background: blanchedalmond;
	}
	.two {
		background: aqua;
	}

	.section-1,
	section-2 {
		padding: 0 1rem;
	}
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin-top: 60px;
	}
</style>
