<script lang="ts">
	let {
		text
	}: {
		text: string;
	} = $props();
</script>

<div class="wave-text">
	<span class="text-purple-500 text-4xl font-semibold">{text}</span>
</div>

<style>
	.wave-text span {
		display: inline-block;
		animation: wave 3s ease-in-out infinite;
	}

	.wave-text span:nth-child(1) {
		animation-delay: 0s;
	}
	.wave-text span:nth-child(2) {
		animation-delay: 0.2s;
	}
	.wave-text span:nth-child(3) {
		animation-delay: 0.4s;
	}
	.wave-text span:nth-child(4) {
		animation-delay: 0.6s;
	}

	@keyframes wave {
		0%,
		100% {
			transform: translateY(0);
		}
		50% {
			transform: translateY(-7px);
		}
	}
</style>
