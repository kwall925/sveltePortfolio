<div class='container'>

  <div class='col1'>
    <h1>Kenneth Wall</h1>
    <p style='color: #d1cfc9'>Front End Developer specializing in Svelte JS</p>
    <button>learn more</button>
    <div class='colInner'>
      <div style="flex:50%">
        <h3>Skills</h3>
        <img src="images/settings.svg">
        <p style="color: #00d4ff">see all</p>
      </div>
      <div style="flex:50%">
        <h3>Contact</h3>
        <img src="images/smartphone.png">
        <p style="color: #00d4ff">leave a message</p>
      </div>
    </div>
  </div>
  <div class='col2'>
    <div class='terminal'>
      <p class='terminalHeader'>main directory</p>
      <div class="css-typing">
        <p>
          <span style='color: #00d4ff'>C:</span> welcome to kens site
        </p>
        <p>
          <span style='color: #00d4ff'>C:</span> navigate the site here or on the top bar:
        </p>
        <p>
          home | skills | recent work | contact
        </p>
      </div>
    </div>
  </div>
</div>

<style>
  .container{
    border: 1px solid black;
    padding: 2em;
    margin:  1em;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    max-width: 1200px;
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
  h1 {
    color:  white;
    text-decoration: underline 5px #00d4ff;
    margin: 0;
    padding: 0;
  }

  h3{
    color:  #d1cfc9;
  }
  .col1{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: start;
    padding:  1.5em;
  }
  .col1 > p {
    font-size: 1.1em;
  }
  .colInner {
    width:100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
  }
  img {
    height:  3em;
    margin: 0;
    padding: 0;
  }
  .col2{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding:  1.5em;

  }
  .terminal{
    background: black;
/*    border: 3px solid lightgrey;
*/    padding: 0 1em;
    height: 500px;
    width: 375px;
  }
  .terminalHeader {
    color: #595959;
    display: flex;
    position:  relative;
    padding:  0;
    margin:  0;
    top: 0;
    justify-content: center;
    width:  100%;
  }
  /* https://codepen.io/Bojoer/pen/EZYgeO */
.css-typing p {
  border-right: .15em solid #00d4ff;
  font-family: "Courier";
  font-size: 14px;
  white-space: nowrap;
  overflow: hidden;
  color:  white;
}
.css-typing p:nth-child(1) {
  width: 15em;
  -webkit-animation: type 2s steps(40, end);
  animation: type 2s steps(40, end);
  -webkit-animation-fill-mode: forwards;
  animation-fill-mode: forwards;
}

.css-typing p:nth-child(2) {
  width: 28em;
  opacity: 0;
  -webkit-animation: type2 2.5s steps(40, end);
  animation: type2 2.5s steps(40, end);
  -webkit-animation-delay: 2s;
  animation-delay: 2s;
  -webkit-animation-fill-mode: forwards;
  animation-fill-mode: forwards;
}

.css-typing p:nth-child(3) {
  width: 23em;
  opacity: 0;
  -webkit-animation: type3 2.5s steps(40, end), blink .5s step-end infinite alternate;
  animation: type3 2.5s steps(20, end), blink .7s step-end infinite alternate;
  -webkit-animation-delay: 4.5s;
  animation-delay: 4.5s;
  -webkit-animation-fill-mode: forwards;
  animation-fill-mode: forwards;
}

@keyframes type {
  0% {
    width: 0;
  }
  99.9% {
    border-right: .15em solid #00d4ff;
  }
  100% {
    border: none;
  }
}

@-webkit-keyframes type {
  0% {
    width: 0;
  }
  99.9% {
    border-right: .15em solid #00d4ff;
  }
  100% {
    border: none;
  }
}

@keyframes type2 {
  0% {
    width: 0;
  }
  1% {
    opacity: 1;
  }
  99.9% {
    border-right: .15em solid #00d4ff;
  }
  100% {
    opacity: 1;
    border: none;
  }
}

@-webkit-keyframes type2 {
  0% {
    width: 0;
  }
  1% {
    opacity: 1;
  }
  99.9% {
    border-right: .15em solid #00d4ff;
  }
  100% {
    opacity: 1;
    border: none;
  }
}

@keyframes type3 {
  0% {
    width: 0;
  }
  1% {
    opacity: 1;
  }
  100% {
    opacity: 1;
  }
}

@-webkit-keyframes type3 {
  0% {
    width: 0;
  }
  1% {
    opacity: 1;
  }
  100% {
    opacity: 1;
  }
}

@keyframes blink {
  50% {
    border-color: transparent;
  }
}
@-webkit-keyframes blink {
  50% {
    border-color: tranparent;
  }
}
</style>
