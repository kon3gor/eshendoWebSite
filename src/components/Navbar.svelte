  <style>

nav{
  position: fixed;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-height: 100px;
  z-index: 1;
  padding-top: 20px;
  padding-bottom: 20px;

}

.nav{
    background-color: transparent;
}

.nav-list{
  display: flex;
  list-style: none;
  justify-content: center;
  margin: 0;
  font-size: 0.7em;
  margin-right: 100px;
}

.nav-link{
  margin-left: 30px;
  position: relative;
  font-size: 2.5em;
  color: black;
  font-family: "VT323", monospace;
  text-decoration: none;
}

.active-color{
  color: black;
}

.inactive-color{
  color: white;
}

.menu-top-color{
  background-color: white;
}

.menu-color{
  background-color: black;
}

#myname{
    margin-top: 0;
    margin-bottom: 0;
    font-size: 3em;
    margin-left: 100px;
    font-family: "VT323", monospace;
    text-decoration: none;
}

a:hover{
  color: #6342bd;
}

.scrolling-active{
  background-color: white;
  box-shadow: 0 3px 1rem rgba(0, 0, 0, .1);
}

.menu-item{
  width: 30px;
  height: 3px;
  margin-top: 5px;
  border-radius: 1px;
}

.menu{
  transform: translate(-100%, 0%);
  height: 24px;
  width: 30px;
  margin-right: 50px;
  display: none;
  cursor: pointer;
}

.nav-list-default{
  background-color: transparent;
}

.nav-list-white{
  background-color: white;
}

.menu-active{
  transform: translateX(100%);
}

.burger-active{
  transform: rotate(45deg) translate(-5.5px, -5.5px);
}

.burger-active2{
  transform: rotate(-45deg) translate(-5px, 6px);
}

@media screen and (max-width: 1300px) {
  .nav-link{
    font-size: 2em;
    margin-left: 20px;
  }
}

@media screen and (max-width: 1150px) {
  .nav-link{
    font-size: 1.7em;
    margin-left: 10px;
  }
}


@media screen and (max-width: 1050px) {
  .nav-list{
    margin-right: 50px;
    position: absolute;
    right: 0px;
    top: 7vh;
    height: 92vh;
    margin-right: 0px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: column;
    width: 100%;
    padding-top: 10px;
    backdrop-filter: blur(4px);
  }

  #myname{
    margin-left: 50px;
    width: 100vw;
  }

  .menu{
    display: block;
  }
  .nav-link{
    color: black;
  }

}

@media screen and (max-width: 600px){
  #myname{
    font-size: 2em;
  }
}


@media screen and (max-width: 481px){
  #myname{
    font-size: 1.5em;
    margin-left: 0px;
    padding-left: 10px;
  }
  .menu{
    margin-right: 0px;
    padding-right: 0px;
  }
}


</style>

<script>
  export let navClass = "nav"
  export let color = "active-color"
  export let menuColor = "menu-top-color"
  export let navListColor = "nav-list-default"

  let burger = 0
  let translated = true
  let active = ""
  let active2 = ""
  let opacity = 1
  let w

  $: {
    console.log(w);
    if (w <= 1050){
      burger = 100
    }else{
      burger = 0
    }
  }

  function clickBurger(){
    if (!translated){
      burger = 100
      translated = true
      active = ""
      active2 = ""
      opacity = 1
    }else{
      burger = 0
      translated = false
      opacity = 0
      active = "burger-active"
      active2 = "burger-active2"
    }

  }
</script>


<svelte:window bind:innerWidth={w}/>


<nav class={navClass}>
    <p id="myname" class="{color}">Mikhail Beskhitrov</p>
    <ul class="nav-list {navListColor}" style="transform: translateX({burger}%)">
        <li>
            <a href="#text" class="nav-link {color}">About</a>
        </li>
        <li>
            <a href="index.html"  class="nav-link {color}">Skills</a>
        </li>
        <li>
            <a href="index.html"  class="nav-link {color}">My way</a>
        </li>
        <li>
            <a href="index.html" class="nav-link {color}">Projects</a>
        </li>
        <li>
            <a href="index.html" class="nav-link {color}">Contacts</a>
        </li>
    </ul>

    <div class="menu" on:click={clickBurger}>
      <div class="menu-item {menuColor} {active2}"></div>
      <div class="menu-item {menuColor}" style="opacity: {opacity}"></div>
      <div class="menu-item {menuColor} {active}"></div>
    </div>
</nav>
