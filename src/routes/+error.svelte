<script lang="ts">
	import { page } from '$app/state';
</script>

<div id="err-wrapper" class="flex justify-center items-center flex-col text-center gap-4">
	<h1 class="text-[48px]">{page.status} error</h1>
	<p>
		Page that you tried to reach is either deleted or it never existed to begin with. <br />You can
		either return to <a href="/" class="font-bold underline underline-offset-4">home page</a> or you
		can check this cool thing called tralalero tralala
	</p>
	<img src="tralalero.gif" alt="brainrot" />
</div>

<style>
	#err-wrapper {
		min-height: 88vh;
	}
</style>
