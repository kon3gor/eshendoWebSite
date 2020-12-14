<div class="container">

    <div class="text-container">

      <h1 class="header">About me</h1>
      <p> Well, I was born on 3 June, 2003. Nothing interesting at all, isn’t it ? I started to learn programming in 2016, when I was in the 7 grade. My first programming language was C++ and, uhhhhh, I used to hate it, but now, when I’ve learnt Python, R, Java, C#, Kotlin, Dart, Go, Js, Scala, Lua and brainfuck (damn it), C++ is not that bad. Now my main languages are Java and Kotlin, because I’m a mobile developer :) But I love programming and I like to use some other languages sommetimes.  For  instance, I could write this site using classic js+html+css, but I’ve chosen something more interesting...AngularDart with Go backend. I think that’s all you need to know, go ahead and explore :)
      </p>
      <div class="img-holder">
        <img alt="it's me :)" src="me.png" id="me">
        <img id="arrow" alt="arrow" src="line2.png">
      </div>

    </div>

    <div class="tube-holder">
      <img id="small" alt=small src="small_tube.png">
    </div>
</div>


<style>
  .container{
    height: 100vh;
    text-align: center;
    display: flex;
    flex-direction: row;
    margin-top: 50px;
  }

  .text-container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin: auto 300px
  }

  .text-container > p{
    font-family: "Ubuntu", monospace;
    color: black;
    font-size: 1.5em;
    text-align: start;
  }

  .img-holder{
    width: 100%;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-direction: row-reverse;
  }

  .tube-holder{
    height: 100%;
    position: relative;
  }

  #arrow{
    max-height: 200px;
    margin-right: 20px;
  }

  #high{
    max-height: 600px;
    position: absolute;
    bottom: 0;
    left: 0;
  }

  #small{
    position: absolute;
    bottom: 0;
    right: 0;
  }


  @media screen and (max-width: 481px){
      .text-container{
        margin-left: 10px;
        margin-right: 10px
      }

      .text-container > p{
        font-size: 1em;
        padding-left: 10px;
        padding-right: 10px
      }

      #arrow{
        width: 150px;
        height: 120px;
      }
      #me{
        height: 200px;
      }
      .tube-holder{
        display: none;
      }
  }



</style>
