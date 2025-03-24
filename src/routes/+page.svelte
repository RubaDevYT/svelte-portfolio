<script lang="ts">
	import CountryCard from './Components/CountryCard.svelte';
	import Wave from './Components/Wave.svelte';
	import Whatsapp from './Components/Whatsapp.svelte';
	import Work from './Components/Work.svelte';

	const githubAccount = 'https://github.com/RubaDevYT';
	const instagramAccount = 'https://www.instagram.com/apsolutan_xyz/';
	let location = 'Split, Croatia';
	let countries = [
		'Italy',
		'China',
		'S. Korea',
		'Serbia',
		'Vatican',
		'Greece',
		'Germany',
		'Austria',
		'Hungary',
		'Romania',
		'BiH'
	];

	let countriesVisited = countries.length;
</script>

<svelte:head>
	<title>KarloRubic.com</title>
</svelte:head>

<div id="app-wrapper" class="flex flex-col bg-cover bg-center bg-[url(/bg.png)]">
	<Work></Work>
	<div class="flex flex-col gap-4 mt-12 text-center items-center">
		<img class="w-[64px]" src="favicon.png" alt="Karlo Rubic" />
		<Wave text="Hi! I am Karlo."></Wave>
		<p>I am Front-End Developer<br /></p>
		<p>I love creating interactive and responsive websites!</p>
		<p>Current location: <span class="font-semibold">{location}</span></p>
		<p>Able to relocate? <span class="font-semibold">Yes</span></p>

		<ul class="flex flex-col gap-4 mt-10">
			<li><p class="text-xl font-semibold">Reach out to me on my socials</p></li>
			<ul class="flex flex-row justify-center items-center gap-4">
				<li>
					<a href={githubAccount} target="_blank"
						><img src="gh.png" alt="karlo rubic github" width="48px" /></a
					>
				</li>
				<li>
					<a href={instagramAccount} target="_blank"
						><img src="ig.png" alt="karlo rubic github" width="48px" /></a
					>
				</li>
			</ul>
		</ul>

		<div class="mt-15 flex justify-center flex-col items-center gap-4">
			<img src="country.png" alt="globe" />
			<p class="font-semibold text-[18px]">I love traveling. It is my biggest passion!</p>
			<p>
				So far I visited {countriesVisited} countries without including my beautiful country
				<span class="font-semibold">Croatia</span> where I was born!
			</p>

			<ul class="flex gap-10 flex-wrap mt-4 justify-center items-center">
				<CountryCard CountryImg="italy.png" CountryName={countries[0]}></CountryCard>
				<CountryCard CountryImg="china.png" CountryName={countries[1]}></CountryCard>
				<CountryCard CountryImg="sk.png" CountryName={countries[2]}></CountryCard>
				<CountryCard CountryImg="serbia.png" CountryName={countries[3]}></CountryCard>
				<CountryCard CountryImg="vatican.png" CountryName={countries[4]}></CountryCard>
				<CountryCard CountryImg="greece.png" CountryName={countries[5]}></CountryCard>
				<CountryCard CountryImg="germany.png" CountryName={countries[6]}></CountryCard>
				<CountryCard CountryImg="austria.png" CountryName={countries[7]}></CountryCard>
				<CountryCard CountryImg="hungary.png" CountryName={countries[8]}></CountryCard>
				<CountryCard CountryImg="romania.png" CountryName={countries[9]}></CountryCard>
				<CountryCard CountryImg="bosnia.png" CountryName={countries[10]}></CountryCard>
			</ul>
		</div>
	</div>
	<Whatsapp></Whatsapp>
</div>

<style>
	#app-wrapper {
		height: 100%;
		min-height: 90vh;
	}
</style>
