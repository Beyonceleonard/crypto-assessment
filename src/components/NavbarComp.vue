<template>
  <nav class="navbar bg-body-tertiary fixed-top">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">SHARENET</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar" aria-controls="offcanvasNavbar" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="offcanvas offcanvas-end" tabindex="-1" id="offcanvasNavbar" aria-labelledby="offcanvasNavbarLabel">
      <div class="offcanvas-header">
        <h5 class="offcanvas-title" id="offcanvasNavbarLabel">SHARENET</h5>
        <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
      </div>
      <div class="offcanvas-body">
        <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#"><router-link to="/">Home</router-link></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"><router-link to="/contact">Contact Us</router-link></a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</nav>
</template>

<style scoped>
.navbar-brand{
  color: #39b3cc !important;
  font-size: 25px;
  font-weight: 300;
  font-family: 'Jost';
}
.navbar{
 height: 70px;
}
</style>

