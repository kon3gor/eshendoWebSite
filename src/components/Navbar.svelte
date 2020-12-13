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

#myname{
    margin-top: 0;
    margin-bottom: 0;
    font-size: 3em;
    margin-left: 100px;
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
  background-color: white;
  height: 3px;
  margin-top: 5px;
}

.menu{
  transform: translate(-100%, 0%);
  height: 24px;
  width: 30px;
  margin-right: 50px;
  display: none;
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
    width: 0px;
    visibility: hidden;
    margin-right: 50px;

  }

  #myname{
    margin-left: 50px;
    width: 100vw;
  }

  .menu{
    display: block; 
  }

}

@media screen and (max-width: 900px) {
  #myname{
    font-size: 2em;
  }
}

@media screen and (max-width: 750px) {
  #myname{
    font-size: 1em;
  }
}

</style>

<script>
  export let navClass = "nav"
  export let color = "active-color"
</script>

<nav class={navClass}>
    <p id="myname" class="nav-link {color}">Mikhail Beskhitrov</p>
    <ul class="nav-list">
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

    <div class="menu">
      <div class="menu-item"></div>
      <div class="menu-item"></div>
      <div class="menu-item"></div>
    </div>
</nav>
