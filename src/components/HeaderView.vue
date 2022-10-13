<template>
  <nav class="navbar navbar-expand-md fixed-top">
        <div class="container position-relative">
        <a class="navbar-brand logo pe-5" href="#">
            <img src="../assets/images/new_logo.svg" alt="">
        </a>

        <div class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar"
          aria-controls="offcanvasNavbar">
          <span class="navbar-toggler-icon"></span>
        </div>

        <div class="offcanvas offcanvas-start" tabindex="-1" id="offcanvasNavbar"
          aria-labelledby="offcanvasNavbarLabel">
          <div class="offcanvas-header">
            <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"></button>
          </div>
          <div class="offcanvas-body">
            <ul class="navbar-nav pe-3">
                <li class="nav-item active">
                    <a class="nav-link p-5" href="#">제이에이코리아</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link p-5" href="#">투명경영</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link p-5" href="#">교육사업</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link p-5" href="#">기관소식</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link p-5" href="#">후원하기</a>
                </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
</template>

<script>
export default {

}
</script>

<style lang="scss">
    .logo{
        img{
            width: 218px;
        }
    }
    .navbar-nav{
        
    }
</style>