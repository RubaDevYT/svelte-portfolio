<script>
	import Header from './Components/Header.svelte';
	import '../app.css';
	import Footer from './Components/Footer.svelte';
</script>

<div class="layout">
	<Header></Header>
	<slot></slot>
	<Footer></Footer>
</div>

<style>
	.layout {
		min-height: 100vh;
		display: flex;
		flex-direction: column;
	}
</style>
