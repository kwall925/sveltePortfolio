<div class='wrapper'>
  <div class="container">
    <h1>About</h1>
    <p>I'm a Front End Developer interested in svelte. Enjoys learning
      new technologies.
      Well versed in HTML, CSS JavaScript. Enjoys buidling front ends.
    </p>

     <p>Currently buidling apps in Svelte and compiling dev knowledge
     that will be published on this site.</p>
  </div>
</div>

<style>
    .wrapper {
    background: #0f0f42;
    display:  flex;
    width:  100%;
    height:  100%;
    justify-content: center;
    align-items: center;
  }
  .container{
    border: 1px solid black;
    padding: 2em;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    max-width: 1200px;
    color:  white;
  }
  @media only screen and (max-width: 767px) {
    .container {
      flex-direction: column;
    }
  }
  @supports (-webkit-backdrop-filter: none) or (backdrop-filter: none) {
  .container {
    -webkit-backdrop-filter: blur(10px);
    backdrop-filter: blur(10px);
    background-color: rgba(255, 255, 255, 0.2);
    /* https://css-tricks.com/almanac/properties/b/backdrop-filter/ */
    }
  }
</style>
