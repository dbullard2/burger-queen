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
            <img src="../assets/burgers/5.png" alt="" class="u-max-full-width" />
            <h5>The Morning After</h5>
            <div class="bottom">
              <h5 class="price">$???</h5>
              <font-awesome-icon icon="shopping-bag" class="big" />
            </div>
          </div>
        </div>
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
</style>
