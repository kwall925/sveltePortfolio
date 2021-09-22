<script>
  import Background from './Background.svelte'
  import Main from './Main.svelte'
</script>
<div class='container'>
  <Main />
</div>
<style>
  .container {
    height: 100%;
    width:  100%;
    display:  flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    background:  #0f0f42;
  }
</style>
