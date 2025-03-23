<script lang="ts">
	let {
		CountryImg,
		CountryName
	}: {
		CountryImg: string;
		CountryName: string;
	} = $props();
</script>

<div class="flex flex-col gap-2 justify-center items-center">
	<img src={CountryImg} alt="{CountryName} flag" width="64px" />
	<p class="font-semibold text-sm">{CountryName}</p>
</div>
