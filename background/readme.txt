## Notes 

1. Controlling background-images | CSS Tutorial:

https://www.youtube.com/watch?v=3T_Jy1CqH9k&list=PLJeX7XxhZzDLNK04U9sqFzfN4C_x746_Z&index=30&t=57s&ab_channel=KevinPowell

codepen: 
https://codepen.io/kevinpowell/pen/abmGBzd

.bg-image {
  outline: 2px solid black;
  // background-size: 50% 50px;
  padding: 20em;
  background-image: 
    url("https://assets.codepen.io/308367/house.jpg"),
    url("https://assets.codepen.io/308367/f47b1-bandeirinha-azul-e-branca-png.png");;
  background-repeat: no-repeat, repeat;
  background-position: right -20% bottom 0px, top left;
  background-size: auto, 10%;
}

This selects all class that have the word "bg-" in them
- allows you to not have to copy the background-image so many times 
[class*="bg-"] {
  background-image: url("https://assets.codepen.io/308367/home-gym.jpg");
  // background-image: url("https://assets.codepen.io/308367/little-one.jpg");
  background-size: cover;
}


Both ways to keep image center in page: 

*note(image is 96x96) 


    <div class="new">
      <div class="center">
        <div class="card">
          <div class="test">

          </div>
          <!-- <img src="images/image-victor.jpg" alt="" class="image-size"> -->
        </div>

      </div>
    </div>

*note that .image-size is absolute to the entire page while .test is relative to the .new class 

.new{
  position: absolute;
  width: 100vw;
  height: 100vh;
}

.image-size{
  width: 96px;
  height: 96px;
  position: absolute;
  top: calc(50vh - 48px);
  left: calc(50vw - 48px);
}

.test{
  background-image: url(images/image-victor.jpg);
  background-repeat: no-repeat;
  width: 100%;
  height: 100%;
  /* easy to position something on the page */
  background-position: center calc(25vh - 48px);
}
