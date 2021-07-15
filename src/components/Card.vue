<template>
	<div class="col-lg-3 col-md-6 col-12 mb-5">
		<div class="card shadow">
			<img
				class="card-img-top"
				:src="imgUrl"
				alt="Card image"
				style="width: 100%"
			/>
			<div class="card-body" @click.prevent="toggleModal">
				<a href="" :class="buttonColor" class="btn w-100 text-center">{{
					movieName
				}}</a>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		props: ['imgUrl', 'movieName', 'buttonColor'],
		methods: {
			toggleModal() {
				// console.log(this.movieName);
				this.$emit('toggleShowModal', { moviename: this.movieName });
			},
		},
	};
</script>

<style></style>
