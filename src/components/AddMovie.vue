<template>
	<h1 class="mt-5">Add Movie</h1>

	<div class="container w-50">
		<div class="mb-3">
			<labe class="form-label">Movie Title</labe>
			<input type="text" class="form-control" placeholder="movie title" />
		</div>
		<div class="mb-3">
			<labe class="form-label">Movie Image Url</labe>
			<input type="email" class="form-control" placeholder="movie Url" />
		</div>
		<div class="mb-3">
			<labe class="form-label">Select Button colour</labe>
			<select class="form-select" aria-label="Default select example">
				<option selected hidden>Select Button</option>
				<option value="1">btn-primary</option>
				<option value="1">btn-warning</option>
				<option value="1">btn-danger</option>
				<option value="1">btn-info</option>
				<option value="1">btn-dark</option>
				<option value="1">btn-success</option>
			</select>
		</div>
		<div class="mb-3">
			<label for="exampleFormControlTextarea1" class="form-label"
				>Movie Description</label
			>
			<textarea class="form-control" rows="3"></textarea>
		</div>
		<div class="col-12">
			<button class="btn btn-primary w-100" type="submit">Submit form</button>
		</div>
	</div>
</template>

<script>
	export default {};
</script>

<style></style>
