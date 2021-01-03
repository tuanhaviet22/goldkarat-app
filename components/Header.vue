<template>
  <header class='header headery-style-1'>
    <div class='header-middle header-top-1'>
      <div class='container'>
        <div class='row no-gutters align-items-center'>
          <div class='col-md-5 col-sm-6 order-lg-1 order-2'>
            <div class='contact-info'>
              <img src='http://goldkarat.tuanha.asia/assets/frontend/img/icons/icon_phone.png' alt='Phone Icon'>
              <p>Gọi ngay<br> Tư vấn miễn phí: {{ config.contact.phone_number }}</p>
            </div>
          </div>
          <div class='col-lg-2 col-12 order-lg-2 order-1 text-center'>
            <a href='http://goldkarat.tuanha.asia' class='logo-box mb-md--30'>
              <img
                :src='config.config.logo_header'
                :alt='config.config.name_website'>
            </a>
          </div>
          <div class='col-lg-5 col-md-7 col-sm-6 order-lg-3 order-3'>
            <div class='header-toolbar'>
              <div class='search-form-wrapper search-hide' style='display: none;'>
                <form action='http://goldkarat.tuanha.asia/tim-kiem' class='search-form'>
                  <input type='text' name='q' id='search' class='search-form__input'
                         placeholder='Nhập thông tin cần tìm...'>
                  <button type='submit' class='search-form__submit'>
                    <i class='icon_search'></i>
                  </button>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class='header-bottom header-top-1 position-relative navigation-wrap fixed-header'>
      <div class='container position-static'>
        <div class='row'>
          <div class='col-12 position-static text-center'>
            <Menu />
          </div>
        </div>
        <div class='row no-gutters'>
          <div class='col-12'>
            <div class='mobile-menu'></div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data: function() {
    return {
      config: []
    }
  },
  async fetch() {
    this.config = await fetch('http://127.0.0.1:8000/api/config', {
      headers: {
        Authorization: 'Bearer YbmIKnLQhdqvr1ZKgPSO0LvH5aVThz5XkHRiRyjjorrervCLJMH3heoGNruo7YIBPqfLB6R505Iv3M9G'
      }
    }).then(response => response.json())
  }
}

</script>

<style>

</style>
