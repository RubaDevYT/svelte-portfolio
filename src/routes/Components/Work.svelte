<script lang="ts">
	let openToWork = true;
</script>

<div class="flex justify-center items-center">
	<div
		class="px-6 py-2 rounded-b-2xl min-w-[200px] text-center"
		style="background-color: {openToWork ? '#42f54e' : '#f54242'}"
	>
		{openToWork ? 'Open to work' : 'Currently not open for work'}
	</div>
</div>

<style>
</style>
