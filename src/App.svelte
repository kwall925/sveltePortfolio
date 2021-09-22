<script>
  import Tabs from "./Tabs.svelte";
	import Home from './home/Home.svelte';
	import Recent from './Recent.svelte';
	import Skills from './skills/Skills.svelte';
  import Bio from './Bio.svelte';
  import Contact from './Contact.svelte';
  // List of tab items with labels and values.
  let tabItems = [
    { label: "Home", value: 1 },
    { label: "Recent", value: 2 },
    { label: "Skills", value: 3 },
    { label: "Bio", value: 4 },
    { label: "Contact", value: 5 }
  ];
  // Current active tab
  let currentTab;
</script>

<Tabs bind:activeTabValue={currentTab} items={tabItems} />

<code class="language-text"></code>
<div class="container">
  {#if 1 === currentTab}
    <Home />
  {/if}
  {#if 2 === currentTab}
    <Recent />
  {/if}
  {#if 3 === currentTab}
    <Skills />
  {/if}
  {#if 4 === currentTab}
    <Bio />
  {/if}
  {#if 5 === currentTab}
    <Contact />
  {/if}
</div>

<style>
	.container {
  	width: 100%;
		height: 100%;
	}
</style>
