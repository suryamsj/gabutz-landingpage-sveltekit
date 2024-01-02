<script>
	export let classId = '';
	export let title = '';
	export let description = '';
</script>

<section class={classId} id={classId}>
	<div class="container">
		<div class="row justify-content-center">
			<div class="col-lg-6 col-md-12 col-12">
				<h1 class="section_title">{title}</h1>
				<p class="section_description">
					{description}
				</p>
			</div>
		</div>
		<slot />
	</div>
</section>
