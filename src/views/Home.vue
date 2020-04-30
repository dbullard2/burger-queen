<template>
  <div class="home" id="home">
    <nav id="navbar">
      <div class="nav-inner">
        <h1><span class="burger">BURGER</span> <span class="queen">Queen</span></h1>
        <div class="nav-middle">
          <h5 style="margin-right: 30px;">Menu</h5>
          <h5 style="margin-right: 30px;">Deals</h5>
          <h5 style="margin-right: 30px;">Specials</h5>
        </div>
        <div class="nav-right">
          <h5>??</h5>
          <font-awesome-icon icon="shopping-bag" style="font-size: 20px" />
        </div>
      </div>
    </nav>

    <div class="container">
      <div class="one">
        <div>
          <h1><span class="burger">BURGER</span> <span class="queen">Queen</span></h1>
          <h5>The burger place taking LA by storm</h5>
        </div>
        <img src="../assets/burgers/classic.png" alt="" class="u-max-full-width" />
      </div>
      <div class="two">
        <h3>The Menu</h3>
        <div class="menu-list">
          <h5>Burgers</h5>
          <h5>Drinks</h5>
          <h5>Sides</h5>
          <h5>Deserts</h5>
        </div>
        <div class="menu">
          <div class="menu-item">
            <img
              src="../assets/burgers/classic (copy 1).png"
              alt=""
              class="u-max-full-width"
            />
            <h5>The Classic</h5>
            <div class="bottom">
              <h5 class="price">$???</h5>
              <font-awesome-icon icon="shopping-bag" class="big" />
            </div>
          </div>
          <div class="menu-item">
            <img src="../assets/burgers/krabby-patty.png" alt="" class="u-max-full-width" />
            <h5>The Krabby Patty</h5>
            <div class="bottom">
              <h5 class="price">$???</h5>
              <font-awesome-icon icon="shopping-bag" class="big" />
            </div>
          </div>
          <div class="menu-item">
            <img src="../assets/burgers/3.png" alt="" class="u-max-full-width" />
            <h5>3</h5>
            <div class="bottom">
              <h5 class="price">$???</h5>
              <font-awesome-icon icon="shopping-bag" class="big" />
            </div>
          </div>
          <div class="menu-item">
            <img src="../assets/burgers/4.png" alt="" class="u-max-full-width" />
            <h5>4</h5>
            <div class="bottom">
              <h5 class="price">$???</h5>
              <font-awesome-icon icon="shopping-bag" class="big" />
            </div>
          </div>
          <div class="menu-item">
            <img src="../assets/burgers/6.png" alt="" class="u-max-full-width" />
            <h5>6</h5>
            <div class="bottom">
              <h5 class="price">$???</h5>
              <font-awesome-icon icon="shopping-bag" class="big" />
            </div>
          </div>
          <div class="menu-item">
            <img src="../assets/burgers/8.png" alt="" class="u-max-full-width" />
            <h5>8</h5>
            <div class="bottom">
              <h5 class="price">$???</h5>
              <font-awesome-icon icon="shopping-bag" class="big" />
            </div>
          </div>
          <div class="menu-item">
            <img src="../assets/burgers/5.png" alt="" class="u-max-full-width" />
            <h5>The Morning After</h5>
            <div class="bottom">
              <h5 class="price">$???</h5>
              <font-awesome-icon icon="shopping-bag" class="big" />
            </div>
          </div>
          <div class="menu-item">
            <img src="../assets/burgers/7.png" alt="" class="u-max-full-width" />
            <h5>7</h5>
            <div class="bottom">
              <h5 class="price">$???</h5>
              <font-awesome-icon icon="shopping-bag" class="big" />
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="container">
      <h3 style="text-align: center">Our App</h3>
      <div class="three">
        <div>
          <div>
            <h5 style="color: #14ff6e; font-weight: bold;">Food</h5>
            <h5>Get nutritional information about our products</h5>
          </div>
        </div>
        <div class="mock">
          <img src="../assets/mobile/x-loading.png" alt="" />
          <img src="../assets/mobile/x-main.png" alt="" />
        </div>
        <div>
          <h5 style="color: #14ff6e; font-weight: bold;">Specials</h5>
          <h5>Learn about all of the specials we have going on</h5>
        </div>
      </div>
      <div class="download">
        <img src="../assets/mobile/app-store.png" alt="" />
        <img src="../assets/mobile/play-store.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

//sticky nav

window.addEventListener('load', function() {
  window.onscroll = () => {
    stick();
  };

  var navbar = document.getElementById('navbar');
  var sticky = navbar.offsetTop;

  function stick() {
    if (window.pageYOffset >= sticky) {
      navbar.classList.add('sticky');
    } else {
      navbar.classList.remove('sticky');
    }
  }
});
</script>

<style scoped>
/* Global */
.nav-inner {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  background-color: #0c0d10;
  overflow: hidden;
}

.home {
  font-family: 'Nunito', sans-serif;
  font-weight: 400;
}

/* Navbar */
.sticky {
  width: 100%;
  position: fixed;
  top: 0;
}

.sticky + container {
  padding-top: 60px;
}

#navbar {
  z-index: 99999999999;
}

.nav-middle {
  display: flex;
  justify-content: space-evenly;
}

.nav-right {
  display: flex;
  margin-right: 60px;
}

/*Section One*/

.one {
  display: flex;
  align-items: center;
  height: 100vh;
}

.one h1 {
  font-size: 7rem;
}

.burger {
  font-family: 'Nunito', sans-serif;
  font-weight: 900;
}

.queen {
  font-family: 'Playfair Display', serif;
  color: #14ff6e;
}

/*Section Two*/
.menu-list {
  display: flex;
  justify-content: space-evenly;
}
.menu {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-column-gap: 50px;
}

.menu-item {
  background-color: #111217;
  text-align: center;
}

.price {
  color: #14ff6e;
  float: left;
}

.big {
  font-size: 20px;
  color: #14ff6e;
  float: right;
}

.three {
  height: 50vh;
  width: 100%;
  display: flex;
  align-items: center;
  flex-basis: 33.3%;
  flex-grow: 0;
}

.mock {
  height: 100%;
  display: flex;
  align-items: center;
  background-image: url('../assets/blob-shape.svg');
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
}

.mock img {
  height: 90%;
}

.download {
  width: 100%;
  display: flex;
  justify-content: center;
}

.download img {
  max-width: 20%;
}
</style>
