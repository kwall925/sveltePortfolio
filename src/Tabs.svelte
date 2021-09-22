<script>
  import { onMount } from "svelte";
  import { fly } from 'svelte/transition';

  export let items = [];
  export let activeTabValue;

  onMount(() => {
    // Set default tab value
    if (Array.isArray(items) && items.length && items[0].value) {
      activeTabValue = items[0].value;
    }
  });

  const handleClick = tabValue => () => (activeTabValue = tabValue);

  // sidebar
  let show = false
</script>

<img src="images/bars.svg" class='expand' alt="click to expand menu" on:click={() => show = !show}>


<ul>
  {#if Array.isArray(items)}
    {#each items as item}
      <li class={activeTabValue === item.value ? 'active' : ''}>
        <span on:click={handleClick(item.value)}>{item.label}</span>
      </li>
    {/each}
  {/if}
</ul>

{#if show}
  <nav transition:fly={{x: 250, opacity: 1}}>
    <img src="images/close.svg" class='close' alt="collapse navigation" on:click={() => show = !show}>
  {#if Array.isArray(items)}
    {#each items as item}
      <li class={activeTabValue === item.value ? 'active' : ''}>
        <span on:click={handleClick(item.value)}>{item.label}</span>
      </li>
    {/each}
  {/if}
  </nav>
{/if}

<style>

  .expand {
    display: none;
    height: 3em;
    margin-bottom: 2em;
    padding:  1em 0 1em 1em;
    z-index: 999;
  }

  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    background: black;
    padding:  0.7em 0;
    margin:  0;
    list-style: none;
  }

  @media only screen and (max-width: 767px) {
    ul {
      display:  none;
    }

    li {
      color:  blue;
      list-style: none;
      font-size: 2em;

    }
    .expand {
      display:  inline-block;
    }
  }

  span {
    display: block;
    padding: 0.5rem 1rem;
    cursor: pointer;
  }

  span:hover {
    border-color: #e9ecef #e9ecef #dee2e6;
  }



  nav {
  position: fixed;
  top: 0;
  right: 0;
  height: 100%;
  padding: 2rem 1rem 0.6rem;
  background: #fff;
  overflow-y: auto;
  width: 17rem;
  z-index:  1000;
}

.close {
  height:  1em;
}

@media only screen and (min-width: 768px) {
  nav {
    display:  none;
  }

    li {
    color: white;
  }

  li.active > span {
    color:  #00d4ff
  }
}
</style>
