<template>
<div>
  <div class="nav-bar" id="nav-bar">
    <div class="inline-block left-nav">
      <img :src="logoSVG" alt="logo" class="logo" />
    </div>
    <div class="inline-block center-nav">
      <div class="nav-center-text">
        <div class=" nav-center-text-left"><a href="#">CAMPAIGNS</a></div>
        <div class=" nav-center-text-center"><a href="#">INFLUENCERS</a></div>
        <div class=" nav-center-text-right"><a href="#">STATISTICS</a></div>
      </div>
    </div>
    <div class="inline-block right-nav">
      <table class="nav-text-left-content-table">
        <td class="nav-text-left-content-td">
          <div class="inline relative">
            <embed class="mail-svg" :src="mailSVG" />
            <embed class="circle-svg" :src="circleSVG" type="" />
            <p class="notification-p">2</p>
          </div>
        </td>
        <td
          style="padding-top: 7px;user-select: none;-moz-user-select: none;-khtml-user-select: none;-webkit-user-select: none;-o-user-select: none;"
        >
          <embed style="height: 33px;" class="nike-normal-svg" :src="nikeSVG" />
        </td>

        <td class="my-profile-p">My Profile</td>
        <td><embed :src="arrowDownSVG" /></td>
      </table>
    </div>
    <div class="menu-bar">
      <i class="fas fa-bars menu-bar-icon" ></i>
    </div>
  </div>
  <div>
    <div class="mobile-nav-bar" id="mobile-nav-bar">
      <div class="nav-bar other-nav-bar" id="nav-bar">
        <div class="inline-block left-nav">
          <img :src="logoSVG" alt="logo" class="logo" />
        </div>
        <div class="inline-block center-nav">
          <div class="nav-center-text">
            <div class=" nav-center-text-left"><a href="#">CAMPAIGNS</a></div>
            <div class=" nav-center-text-center">
              <a href="#">INFLUENCERS</a>
            </div>
            <div class=" nav-center-text-right"><a href="#">STATISTICS</a></div>
          </div>
        </div>
        <div class="inline-block right-nav">
          <table class="nav-text-left-content-table">
            <td class="nav-text-left-content-td">
              <div class="inline relative">
                <embed class="mail-svg" :src="mailSVG" />
                <embed class="circle-svg" :src="circleSVG" type="" />
                <p class="notification-p">2</p>
              </div>
            </td>
            <td
              style="padding-top: 7px;user-select: none;-moz-user-select: none;-khtml-user-select: none;-webkit-user-select: none;-o-user-select: none;"
            >
              <embed style="height: 33px;" :src="nikeSVG" />
            </td>

            <td class="my-profile-p">My Profile</td>
            <td><embed :src="arrowDownSVG" /></td>
          </table>
        </div>
        <div class="menu-bar">
          <i class="fas fa-bars menu-bar-icon" ></i>
        </div>
      </div>
      <div class="dropdown-upper"> 
        <table class="nav-text-left-content-table">
          <td class="nav-text-left-content-td">
            <div class="inline relative">
              <embed class="mail-svg" :src="mailSVG" />
              <embed class="circle-svg" :src="circleSVG" type="" />
              <p class="notification-p">2</p>
            </div>
          </td>
          <td class="nike-svg-td">
            <embed class="nike-svg" :src="nikeSVG" />
          </td>

          <td class="my-profile-p">My Profile</td>
          <td><embed :src="arrowDownSVG" /></td>
        </table>
      </div>
      <div class="dropdown-content">
        <div class="mobile-nav-item">
          <a href="#">CAMPAIGNS</a>
        </div>
        <div class="mobile-nav-item">
          <a href="#">INFLUENCERS</a>
        </div>
        <div class="mobile-nav-item">
          <a href="#">STATISTICS</a>
        </div>
      </div>
    </div>
  </div>
  </div>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      arrowDownSVG: require("../assets/svg/arrow-down.svg"),
      circleSVG: require("../assets/svg/circle.svg"),
      logoSVG: require("../assets/svg/logo.svg"),
      mailSVG: require("../assets/svg/mail.svg"),
      nikeSVG: require("../assets/svg/nike.svg"),
    };
  }
};

</script>
<style>
.nav-bar {
  margin: 0px;
  min-height: 70px;
  display: table;
  min-width: 100%;
  position: fixed;
  z-index:999;
  background-color:#FFFFFF;
}
.nike-normal-svg{
  position:absolute;
  display:block;

}

#nav-bar {
  box-shadow: 6px 3px 6px 3px #888888;
}

body {
  margin: 0;
  font-family: "Lato", sans-serif;
  font-size: 20px;
  background-color: white;
  margin:0;
}

.inline-block {
  display: inline-block;
}

.logo {
  margin-left: 30px;
  width: 85px;
  height: 29px;
  transition: 0.2s;
  margin-top: 5px;
  user-select: none;
  -moz-user-select: none;
  -khtml-user-select: none;
  -webkit-user-select: none;
  -o-user-select: none;
}

.logo:hover {
  opacity: 50%;
  transition: 0.2s;
}

@media screen and (min-width: 1150px) {
  .right-nav {
    display: table-cell;
    /* min-width: 9vmin; */
    vertical-align: middle;
    width: 33%;
  }

  .left-nav {
    display: table-cell;
    vertical-align: middle;
    /* min-width: 9vmin; */
    width: 33%;
  }

  .center-nav {
    display: table-cell;
    text-align: center;
    vertical-align: middle;
    /* min-width: 9vmin; */
    width: 33%;
  }

  .main {
    margin-top: 100px;
  }

  .nav-center-text-center {
    margin-left: 2%;
    margin-right: 2%;
  }

  .nav-center-text-left {
    display: inline-block;
  }

  .nav-center-text-center {
    display: inline-block;
  }

  .nav-center-text-right {
    display: inline-block;
  }

  .menu-bar {
    visibility: hidden;
    font-size: 30px;
    display: none;
  }

  .menu-bar-icon {
    transition: 0.3s;
    cursor: pointer;
    margin: 20px;
  }

  .mobile-nav-bar {
    display: none;
  }
}

@media screen and (min-width: 775px) and (max-width: 1150px) {
  .right-nav {
    display: table-cell;
    /* min-width: 9vmin; */
    vertical-align: middle;
    width: 20%;
    /* text-align: center; */
  }

  .left-nav {
    display: table-cell;
    vertical-align: middle;
    /* min-width: 9vmin; */
    width: 20%;
  }

  .center-nav {
    display: table-cell;
    text-align: center;
    vertical-align: middle;
    /* min-width: 9vmin; */
    width: 60%;
  }

  .main {
    margin-top: 100px;
  }

  .nav-center-text-center {
    margin-left: 2%;
    margin-right: 2%;
  }

  .nav-center-text-left {
    display: inline-block;
  }

  .nav-center-text-center {
    display: inline-block;
  }

  .nav-center-text-right {
    display: inline-block;
  }

  .menu-bar {
    visibility: hidden;
    font-size: 30px;
    display: none;
  }

  .menu-bar-icon {
    transition: 0.3s;
    cursor: pointer;
    margin: 20px;
  }

  .mobile-nav-bar {
    display: none;
  }
}

@media screen and (min-width: 0px) and (max-width: 775px) {
  .right-nav {
    display: none;
  }

  .left-nav {
    display: table-cell;
    vertical-align: middle;
    width: 20%;
  }

  .center-nav {
    display: none;
  }

  .main {
    margin-top: 100px;
  }

  .nav-center-text-center {
    margin-left: 2%;
    margin-right: 2%;
  }

  .nav-center-text-left {
    display: inline-block;
  }

  .nav-center-text-center {
    display: inline-block;
  }

  .nav-center-text-right {
    display: inline-block;
  }

  .menu-bar {
    float: right;
    font-size: 30px;
    /* min-width: 9vmin; */
    /* width: 20%; */
  }

  .menu-bar-icon {
    transition: 0.3s;
    cursor: pointer;
    margin: 20px;
    display: block;
  }

  .menu-bar-icon:hover {
    opacity: 50%;
    transition: 0.3s;
  }
}

a {
  text-decoration: none;
  color: black;
  transition: 0.2s;
}

a:hover {
  opacity: 50%;
  transition: 0.2s;
}

.inline {
  display: inline;
}

.arrow-down {
  margin-left: 3px;
  user-select: none;
  -moz-user-select: none;
  -khtml-user-select: none;
  -webkit-user-select: none;
  -o-user-select: none;
}

.nav-text-left-content-table {
  width: auto;
  margin-right: 40px;
  margin-left: auto;
}

.nav-text-left-content-td {
  padding-top: 7px;
  padding-right: 10px;
}

.relative {
  position: relative;
}

.mail-svg {
  height: 22px;
  position: absolute;
  bottom: 0px;
  right: 0px;
  user-select: none;
  -moz-user-select: none;
  -khtml-user-select: none;
  -webkit-user-select: none;
  -o-user-select: none;
}

.circle-svg {
  position: absolute;
  bottom: -11px;
  right: -6px;
  height: 17px;
  user-select: none;
  -moz-user-select: none;
  -khtml-user-select: none;
  -webkit-user-select: none;
  -o-user-select: none;
}

.notification-p {
  position: absolute;
  bottom: -26px;
  right: -1px;
  font-size: 11px;
  font-weight: 700;
  color: magenta;
  user-select: none;
  -moz-user-select: none;
  -khtml-user-select: none;
  -webkit-user-select: none;
  -o-user-select: none;
}

.my-profile {
  user-select: none;
  -moz-user-select: none;
  -khtml-user-select: none;
  -webkit-user-select: none;
  -o-user-select: none;
}

#mobile-nav-bar {
  width: 100%;
  height: 0px;
  position: fixed;
  /* position: relative; */
  z-index: 1;
  top: 0;
  left: 0;
  /* background-color: rgb(252, 252, 252); */
  background-color: white;
  overflow-x: hidden;
  transition: 0.5s;
  /* padding: 60px; */
  /* margin-top: 71px; */
  overflow-y: hidden;
  visibility: hidden;
  font-size: 40px;
  /* top: 100px; */
}

.other-nav-bar {
  background-color: white;
}

.dropdown-content {
  /* padding-top: 90px; */
  padding-left: 30px;
}

.mobile-nav-item {
  margin-top: 50px;
}

.dropdown-upper {
  overflow: hidden;
  /* position: relative; */
  bottom: 0;
  width: 100%;
  font-size: 30px;
  margin-top: 73px;
  float: left;
  /* background-color: lightgray; */
}

.nike-svg {
  position:absolute;
}

.nike-svg-td {
  padding-top: 0px;
  position:absolute;
  bottom:0px;
  user-select: none;
  -moz-user-select: none;
  -khtml-user-select: none;
  -webkit-user-select: none;
  -o-user-select: none;
}
</style>
