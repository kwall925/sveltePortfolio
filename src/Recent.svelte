<script>
  import { fade } from 'svelte/transition';

  async function fetchData() {
    const res = await fetch("https://api.github.com/users/kwall925/repos");
    const data = await res.json();

    if (res.ok) {
      return data;
    } else {
      throw new Error(data);
    }
  }
</script>

<div class="wrapper">
  <div class="container">
    {#await fetchData()}
      <p>connecting to gitHub</p>
    {:then items }
      {#each items as item}
        <div class='content' in:fade>
        <h2>{item.name}</h2>
          {#if item.description}

            <span>"</span>
            {item.description}
            <span>"</span>
          {/if}
          {#if item.language}
            <h5 class='lang'>{item.language}</h5>
            <h5>{item.updated_at.substring(0,10)}</h5>
          {/if}
          <a href="{item.html_url}">view</a>
        </div>
      {/each}
    {:catch error}
      <p style="color: red">{error.message}</p>
    {/await}
  </div>
</div>

<style>
  .wrapper {
    background: #0f0f42;
    display:  flex;
    width:  100%;
    height:  100%;
    justify-content: center;
  }
  .container {
    padding:  1.5em;
    color:  white;
    display: flex;
    flex-wrap: wrap;
  }
    @media (min-width:801px)  {

    .wrapper {

    }
  }

  .content {
    margin:  1em;
    padding:  0.5em;
    max-width: 350px;
    max-height: 400px;
    border:  1px solid black;
  }
  .content:hover {
    box-shadow: 5px 5px 5px  grey;
  }
  @supports (-webkit-backdrop-filter: none) or (backdrop-filter: none) {
  .content {
    -webkit-backdrop-filter: blur(10px);
    backdrop-filter: blur(10px);
    background-color: rgba(255, 255, 255, 0.2);
    /* https://css-tricks.com/almanac/properties/b/backdrop-filter/ */
    }
  }
  .content > * {
    margin:  0;
    padding:  0;
  }
  span {
    font-size: 1.5;
  }
  .lang {
    font-size: .8em;
    font-style: italic;
    font-weight: 200;
  }
  a {
    color: #00d4ff;
  }
</style>
