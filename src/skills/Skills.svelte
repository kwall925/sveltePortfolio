

<script>
     let skillsObj = [
    { 'name' : 'javascript', 'description' : 'es6', 'image' : 'images/js.svg'},
    { 'name' : 'css', 'description' : 'blahblahblah', 'image' : 'images/css.svg'},
    { 'name' : 'html', 'description' : 'html5', 'image' : 'images/html5.svg'},
    { 'name' : 'java', 'description' : 'used to build android apps, exposure to kotlin as well', 'image' : 'images/js.svg'},
    { 'name' : 'node.js', 'description' : 'back end js experience', 'image' : 'images/node.svg'},
    { 'name' : 'frameworks', 'description' : 'react and svelte', 'image' : 'images/react.svg'},
    { 'name' : 'ruby', 'description' : 'in full stack web dev', 'image' : 'images/ruby.svg'},
    { 'name' : 'sass', 'description' : 'and exposure to other CSS tools', 'image' : 'images/sass.svg'},
    { 'name' : 'tools', 'description' : 'npm, vscode, github, android studio', 'image' : 'images/settings.svg'},
    { 'name' : 'SQL', 'description' : 'used in full stack web dev', 'image' : 'images/database-solid.svg'}
  ]
</script>


<div class="container">
        {#each skillsObj as skill}
        <div class="col">
          <h2>{skill.name}</h2>
          <p>{skill.description}</p>
          <img src="{skill.image}" alt="javascript">
        </div>
        {/each}
 </div>

<style>
  .container {
    background: #0f0f42;
    height:  100%;
    width:  100%;
  }
  .col {
    display: inline-block;
    padding: 1em;
    margin:  1em;
  }
    @supports (-webkit-backdrop-filter: none) or (backdrop-filter: none) {
  .col {
    -webkit-backdrop-filter: blur(10px);
    backdrop-filter: blur(10px);
    background-color: rgba(255, 255, 255, 0.2);
    /* https://css-tricks.com/almanac/properties/b/backdrop-filter/ */
    }
  }
  h2{
    text-decoration: underline 4px #00d4ff;
;
  }
  h2, p {
    color:  white;
  }
  img {
    height: 3em;
    color: white;
  }
</style>
