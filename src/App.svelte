<script>
  export let name;
  import Navbar from './components/Navbar.svelte'
  import About from './components/About.svelte'


  let navClass = "nav"
  let color = "inactive-color"
  let menuColor = "menu-top-color"
  let nav = "nav-list-default"

  function changeClass(event){
      let n = event.target.scrollTop
      if (n > 0){
        navClass= "scrolling-active"
        color = "active-color"
        menuColor =  "menu-color"
        nav = "nav-list-white"
      }else{
        navClass = "nav"
        color = "inactive-color"
        menuColor =  "menu-top-color"
        nav = "nav-list-default"
      }
  }


</script>


<main on:scroll={changeClass}>
  <Navbar navClass={navClass} color={color} menuColor={menuColor} navListColor={nav}/>
  <div class="container">
      <img class="cover" src="waffle.gif">
      <div id="welcome"><h1 >Welcome</h1></div>
  </div>
  <div id="text">
    <About/>
  </div>
</main>


<style>

  @import url('https://fonts.googleapis.com/css2?family=VT323&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Ubuntu&display=swap');

	main {
		padding: 0px;
    margin: 0px;
    width: 100%;
    height: 100%;
    box-sizing: border-box;
    overflow-x: hidden;
	}

  :global(body){
    padding: 0;
  }

  .container {
      position: relative;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
  }

  .cover {
      width:100%;
      height:100%;
  }

  #text{
    height: 100vh;
    width: 100%;
    background-color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  #welcome{
    position: absolute;
    color: white;
  }

  #welcome > h1{
    font-family: "VT323";
    font-size: 9em;
  }

  :global(.header){
    font-family: "VT323";
    font-size: 6em;
    color: black;
    text-align: center;
  }

  @media screen and (max-width: 481px){
    #welcome > h1{
      font-size: 7em;
    }
    :global(.header){
      font-size: 5em;
    }
  }

</style>
