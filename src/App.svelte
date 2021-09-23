<script>

	// Components
	import Footer from './components/Footer.svelte';
	import Header from "./components/Header.svelte";
	import SecChef from './components/Sec-chef.svelte'
	import SecHome from "./components/Sec-home.svelte";
	import SecAbout from "./components/Sec-about.svelte";
	import SecHistory from './components/Sec-history.svelte';
	import SecWine from './components/Sec-wine.svelte';

</script>

<div class={`Content_Wrapper`} data-type="Wrapper" >
	<Header />
	<SecHome />
	<SecAbout />
	<SecHistory />
	<SecChef />
	<SecWine />
	<Footer />
</div>

<style>

	.Content_Wrapper {
		display: flex;
		align-items: center;
		flex-direction: column;
		justify-content: center;
	}

</style>