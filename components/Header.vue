<template>
  <header class="header headery-style-1">
    <div class="header-middle header-top-1">
      <div class="container">
        <div class="row no-gutters align-items-center">
          <div class="col-md-5 col-sm-6 order-lg-1 order-2">
            <div class="contact-info">
              <img src="http://goldkarat.tuanha.asia/assets/frontend/img/icons/icon_phone.png" alt="Phone Icon">
              <p>Gọi ngay<br> Tư vấn miễn phí: 0111222333</p>
            </div>
          </div>
          <div class="col-lg-2 col-12 order-lg-2 order-1 text-center">
            <a href="http://goldkarat.tuanha.asia" class="logo-box mb-md--30">
              <img
                src="http://goldkarat.tuanha.asia/storage/photos/1/Banner/logo-dien-thoai-vertu-cong-ty-tnhh-ky-nghe-kim-hoan-goldkarat3.png"
                alt="GoldKarat - Nâng tầm đẳng cấp">
            </a>
          </div>
          <div class="col-lg-5 col-md-7 col-sm-6 order-lg-3 order-3">
            <div class="header-toolbar">
              <div class="search-form-wrapper search-hide" style="display: none;">
                <form action="http://goldkarat.tuanha.asia/tim-kiem" class="search-form">
                  <input type="text" name="q" id="search" class="search-form__input"
                    placeholder="Nhập thông tin cần tìm...">
                  <button type="submit" class="search-form__submit">
                    <i class="icon_search"></i>
                  </button>
                </form>
              </div>
              <ul class="header-toolbar-icons">
                <li class="search-box">
                  <a href="#" class="bordered-icon search-btn" aria-expanded="false"><i class="icon_search"></i></a>
                </li>
                <li class="mini-cart-icon" id="cart-block">
                  <div class="mini-cart mini-cart--1">
                    <a class="mini-cart__dropdown-toggle bordered-icon" id="cartDropdown">
                      <span class="mini-cart__count">0</span>
                      <i class="icon_cart_alt mini-cart__icon"></i>
                      <span class="mini-cart__ammount">0 sản phẩm&nbsp;<i class="fa fa-angle-down"></i></span>
                    </a>
                    <div class="mini-cart__dropdown-menu">
                      <div class="text-center mt-5 mb-5">Giỏ hàng trống</div>
                    </div>
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="header-bottom header-top-1 position-relative navigation-wrap fixed-header">
      <div class="container position-static">
        <div class="row">
          <div class="col-12 position-static text-center">
            <nav class="main-navigation" style="display: block;">
              <ul class="mainmenu">
                <li class="mainmenu__item ">
                  <a href="/" class="mainmenu__link">Trang Chủ</a>
                </li>
                <li class="mainmenu__item ">
                  <a href="http://goldkarat.tuanha.asia/cong-ty-tnhh-ky-nghe-kim-hoan-goldkarat-ld14"
                    class="mainmenu__link">Giới Thiệu</a>
                </li>
                <li class="mainmenu__item ">
                  <a href="http://goldkarat.tuanha.asia/dien-thoai-vertu-ca31.html" class="mainmenu__link">Điện Thoại
                    Vertu</a>
                </li>
                <li class="mainmenu__item ">
                  <a href="http://goldkarat.tuanha.asia/dong-ho-ca32.html" class="mainmenu__link">Đồng Hồ</a>
                </li>
                <li class="mainmenu__item ">
                  <a href="http://goldkarat.tuanha.asia/trang-suc-ca33.html" class="mainmenu__link">Trang Sức</a>
                </li>
                <li class="mainmenu__item ">
                  <a href="http://goldkarat.tuanha.asia/dich-vu-ca46.html" class="mainmenu__link">Dịch Vụ</a>
                </li>
                <li class="mainmenu__item  menu-item-has-children ">
                  <a href="http://goldkarat.tuanha.asia/bo-suu-tap-ca37.html" class="mainmenu__link">Bộ Sưu Tập</a>
                  <ul class="megamenu five-column">
                    <li class="has-children">
                      <a class="megamenu-title" href="http://goldkarat.tuanha.asia/bo-suu-tap-anh-ca30.html">Bộ Sưu Tập
                        Ảnh</a>
                      <ul>
                        <li>
                          <a href="http://goldkarat.tuanha.asia/album-dien-thoai-vertu-nguyen-ban-ca38.html">Album Điện
                            Thoại Vertu Nguyên Bản</a>
                        </li>
                        <li>
                          <a href="http://goldkarat.tuanha.asia/album-dien-thoai-vertu-che-tac-ca39.html">Album Điện
                            Thoại Vertu Chế Tác</a>
                        </li>
                        <li>
                          <a href="http://goldkarat.tuanha.asia/album-dong-ho-ca43.html">Album Đồng Hồ</a>
                        </li>
                        <li>
                          <a href="http://goldkarat.tuanha.asia/album-trang-suc-ca44.html">Album Trang Sức</a>
                        </li>
                      </ul>
                    </li>
                    <li class="has-children">
                      <a class="megamenu-title" href="http://goldkarat.tuanha.asia/bo-suu-tap-video-ca36.html">Bộ Sưu
                        Tập Video</a>
                      <ul>
                        <li>
                          <a href="http://goldkarat.tuanha.asia/video-dien-thoai-vertu-nguyen-ban-ca41.html">Video Điện
                            Thoại Vertu Nguyên Bản</a>
                        </li>
                        <li>
                          <a href="http://goldkarat.tuanha.asia/video-dien-thoai-vertu-che-tac-ca40.html">Video Điện
                            Thoại Vertu Chế Tác</a>
                        </li>
                        <li>
                          <a href="http://goldkarat.tuanha.asia/video-dong-ho-ca42.html">Video Đồng Hồ</a>
                        </li>
                        <li>
                          <a href="http://goldkarat.tuanha.asia/video-trang-suc-ca45.html">Video Trang Sức</a>
                        </li>
                      </ul>
                    </li>
                  </ul>
                </li>
                <li class="mainmenu__item ">
                  <a href="http://goldkarat.tuanha.asia/tin-tuc-ca29.html" class="mainmenu__link">Tin Tức</a>
                </li>
                <li class="mainmenu__item ">
                  <a href="http://goldkarat.tuanha.asia/lien-he" class="mainmenu__link">Liên Hệ</a>
                </li>
              </ul>
            </nav>
          </div>
        </div>
        <div class="row no-gutters">
          <div class="col-12">
            <div class="mobile-menu"></div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
  export default {

  }

</script>

<style>

</style>
