<script>
  let wineImg = "/images/b-1.jpg";
  let friendsImg = "/images/b-2.jpg";
  let desertsImg = "/images/b-3.jpg";
  let cheersImg = "/images/b-4.jpg";
  let foodImg = "/images/b-5.jpg";
  let beerImg = "/images/b-6.jpg";
  // const modal = document.getElementById("myModal");
  // const img = document.getElementsByClassName("myImg");
  // const modalImg = document.getElementById("img01");

  // for (let i = 0; i < img.length; i++) {
  //   img[i].onclick = function () {
  //     modal.style.display = "block";
  //     modalImg.src = this.src;
  //   };
  //  }

  // // span tag to close the picture
  // const span = document.getElementsByClassName("close")[0];

  // span.onclick = () => {
  //   modal.style.display = "none";
  // };
</script>

<!-- Food pics -->

<div class="food-images">
  <div>
    <img class="f-1 myImg" src={wineImg} alt="Wine" />
  </div>
  <div>
    <img class="f-2 myImg" src={friendsImg} alt="friends" />
  </div>
  <div>
    <img class="f-3 myImg" src={desertsImg} alt="desert" />
  </div>
  <div>
    <img class="f-4 myImg" src={cheersImg} alt="cheers" />
  </div>
  <div>
    <img class="f-5 myImg" src={foodImg} alt="food" />
  </div>
  <div>
    <img class="f-6 myImg" src={beerImg} alt="beer" />
  </div>
</div>
<!-- The Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01" alt="img"/>
  <div id="caption" />
</div>

<!--Inside the bar picture -->
<div class="bar-picture">
  <div class="layer" />
  <h3 class="text-uppercase" id="booking">Book an area</h3>
  <button class="btn-two m-2 text-uppercase">Make a booking</button>
  <h3 class="text-uppercase">Here the whole bar?</h3>
  <button class="btn-three m-2 text-uppercase">Private hire enquiry</button>
</div>

<!-- operating hours section -->

<div class="container text-center p-9">
  <h1 class="text-uppercase">Make a booking</h1>
  <button class="btn-four m-2 text-uppercase">Book now</button>
  <h1 class="text-uppercase m-5">Opening times</h1>
  <p class="text-uppercase">Monday: Closed</p>
  <p class="text-uppercase">Tuesday - Saturday: 11:30am - 11pm</p>
  <p class="text-uppercase">Sunday: Closed</p>
  <h1 class="text-uppercase m-5">Contact</h1>
  <p class="text-uppercase">96 ISABELLA ST, LONDON SE1 8DD</p>
  <p class="text-uppercase">TEL: 020 7928 0678</p>
  <button class="btn-five m-2 text-uppercase">Email</button>
</div>

<!-- food grid pics -->
<div class="grid-food" id="selection">
  <div class="gf-1" />
  <div class="gf-2" />
  <div class="gf-3" />
  <div class="gf-4" />
  <div class="gf-5" />
  <div class="gf-6" />
  <div class="gf-7" />
  <div class="gf-8" />
</div>
