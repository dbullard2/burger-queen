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
          <div class="space"></div>
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
        <h3 style="text-align: center">The Menu</h3>
        <div class="menu-list">
          <h5 id="burgers">Burgers</h5>
          <h5>Drinks</h5>
          <h5>Sides</h5>
          <h5>Deserts</h5>
        </div>
        <div class="menu">
          <Sides />
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
    <div class="line"></div>
    <div class="container">
      <div class="four">
        <ul>
          <li><h5 style="color: #14ff6e; font-weight: bold;">Food</h5></li>
          <li><h5>Our History</h5></li>
          <li><h5>The Team</h5></li>
          <li><h5>Values</h5></li>
          <li><h5></h5></li>
        </ul>
        <ul>
          <li><h5 style="color: #14ff6e; font-weight: bold;">Careers</h5></li>
          <li><h5>Education Opportunities</h5></li>
          <li><h5>Employee Perks</h5></li>
          <li><h5>Working With Us</h5></li>
          <li><h5>Apply Now</h5></li>
        </ul>
        <ul>
          <li><h5 style="color: #14ff6e; font-weight: bold;">Contact Us</h5></li>
          <li><h5>Website Feedback</h5></li>
          <li><h5>Mobile App Feedback</h5></li>
          <li><h5>Restaurant Feedback</h5></li>
        </ul>
      </div>
    </div>
    <footer class="footer">
      <p>© Burger Queen, 2020</p>
      <div class="footer-middle">
        <p>Privacy</p>
        <p>Terms & Conditions</p>
        <p>Accessibility</p>
      </div>
      <div class="socials">
        <font-awesome-icon :icon="['fab', 'twitter']" class="big twitter" />
        <font-awesome-icon :icon="['fab', 'facebook-f']" class="big facebook" />
        <font-awesome-icon :icon="['fab', 'youtube']" class="big youtube" />
        <font-awesome-icon :icon="['fab', 'instagram']" class="big instagram" />
      </div>
    </footer>
  </div>
</template>

<script>
// @ is an alias to /src
//import Burgers from '../components/Burgers';
import Sides from '../components/Sides';

export default {
  name: 'Home',
  components: {
    //Burgers,
    //Drinks,
    Sides,
  },
};

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

<style>
/* Global */
ul {
  list-style: none;
}

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
}

.space {
  width: 15px;
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
.burger-menu {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-column-gap: 50px;
  grid-row-gap: 20px;
  width: 100%;
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

.line {
  border-bottom: 3px solid #14ff6e;
  width: 99vw;
  height: 3px;
  margin-top: 30px;
}

.four {
  margin-top: 30px;
  color: #acacac;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-column-gap: 50px;
  justify-items: center;
}

/* Footer */
footer {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-column-gap: 50px;
  justify-items: center;
}

.footer-middle {
  display: flex;
}

.footer-middle p {
  margin-right: 30px;
}

.footer .big {
  color: #fff;
  margin-right: 20px;
}

.footer .big:hover {
  cursor: pointer;
}

.socials {
  display: flex;
}

.twitter:hover {
  color: #1da1f3;
}

.facebook:hover {
  color: #1778f2;
}

.youtube:hover {
  color: #ff0000;
}

.instagram:hover {
  background: #f09433;
  background: -moz-linear-gradient(
    45deg,
    #f09433 0%,
    #e6683c 25%,
    #dc2743 50%,
    #cc2366 75%,
    #bc1888 100%
  );
  background: -webkit-linear-gradient(
    45deg,
    #f09433 0%,
    #e6683c 25%,
    #dc2743 50%,
    #cc2366 75%,
    #bc1888 100%
  );
  background: linear-gradient(
    45deg,
    #f09433 0%,
    #e6683c 25%,
    #dc2743 50%,
    #cc2366 75%,
    #bc1888 100%
  );
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#f09433', endColorstr='#bc1888',GradientType=1 );
}
</style>
