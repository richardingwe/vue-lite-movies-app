<template>
	<h1 class="mt-5">Add Movie</h1>

	<form @submit.prevent="submitMovie" class="container w-50">
		<div class="mb-3">
			<labe class="form-label">Movie Title</labe>
			<input
				type="text"
				class="form-control"
				v-model="movieTitle"
				placeholder="movie title"
				required
			/>
		</div>
		<div class="mb-3">
			<labe class="form-label">Movie Image Url</labe>
			<input
				type="text"
				class="form-control"
				v-model="imgUrl"
				placeholder="movie Url"
				required
			/>
		</div>
		<div class="mb-3">
			<labe class="form-label">Select Button colour</labe>
			<select
				class="form-select"
				v-model="btnColor"
				aria-label="Default select example"
				required
			>
				<option selected hidden>Select Button</option>
				<option>btn-primary</option>
				<option>btn-warning</option>
				<option>btn-danger</option>
				<option>btn-info</option>
				<option>btn-dark</option>
				<option>btn-success</option>
			</select>
		</div>
		<div class="mb-3">
			<label for="exampleFormControlTextarea1" class="form-label"
				>Movie Description</label
			>
			<textarea
				class="form-control"
				v-model="desc"
				rows="3"
				required
			></textarea>
		</div>
		<div class="col-12">
			<button class="btn btn-primary w-100" type="submit">
				Submit form
			</button>
		</div>
	</form>
</template>

<script>
	export default {
		methods: {
			submitMovie() {
				this.$emit('getNewMovie', {
					movieName: this.movieTitle,
					imgUrl: this.imgUrl,
					buttonColor: this.btnColor,
					desc: this.desc,
				});
				this.movieTitle = '';
				this.imgUrl = '';
				this.btnColor = 'btn-primary';
				this.desc = '';
			},
		},
		data() {
			return {
				movieTitle: '',
				imgUrl: '',
				btnColor: 'btn-primary',
				desc: '',
			};
		},
	};
</script>

<style></style>
