
<div class="wrapper">
  <form name="contact" method="POST" netlify-honeypot="bot-field" data-netlify="true">
    <h1>Contact Me</h1>

    <label>Name</label>
    <input name="name" placeholder="First Last" />

    <label>Email</label>
    <input name="email" placeholder="name@example.com" />

    <label>Message</label>
    <textarea></textarea>

    <button type="submit">Submit</button>
  </form>
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

  form {
    transform-origin: 0;
    padding: 50px;
    width: 325px;
    height: 500px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
/*    box-shadow: 0px 3px 15px rgba(250, 250, 250, 0.5);
*/  }
  @supports (-webkit-backdrop-filter: none) or (backdrop-filter: none) {
    form {
        -webkit-backdrop-filter: blur(10px);
        backdrop-filter: blur(10px);
        background-color: rgba(255, 255, 255, 0.2);
      }
      input, textarea {
        -webkit-backdrop-filter: blur(10px);
        backdrop-filter: blur(10px);
        background-color: rgba(255, 255, 255, 0.4);
      }
  }
  label {
    margin: 10px 0;
    align-self: flex-start;
    font-weight: 500;
  }
  input, textarea {
    border: none;
    border-bottom: 1px solid #ccc;
    margin-bottom: 20px;
    transition: all 300ms ease-in-out;
    width: 100%;
  }
  input:focus {
    outline: 0;
    border-bottom: 1px solid #666;
  }
  textarea:focus {
    outline: 0;
    border-bottom: 1px solid #666;
  }
/*  .message{
    height: 100px;
  }*/
  button {
    margin-top: 20px;
    background: black;
    color: white;
    padding: 10px 0;
    width: 200px;
    border-radius: 25px;
    text-transform: uppercase;
    font-weight: bold;
    cursor: pointer;
    transition: all 300ms ease-in-out;
  }
  button:hover {
    transform: translateY(-2.5px);
    box-shadow: 0px 1px 10px 0px rgba(0, 0, 0, 0.58);
  }
  h1 {
    margin: 10px 20px 30px 20px;
    font-size: 38px;
  }
</style>
