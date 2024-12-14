<template>
  <div class="container text-center">
    <div class="row" style="margin-top: 2rem; margin-bottom: 1rem;"></div>
    <div class="row">
      <div class="col-md-12 mb-1">
        <img width="150px" src="/public/assets/images/logo.jpg" alt="">
        <h1 style="font-family: Tahrir;margin-bottom: 5rem;">شهرداری قمصر </h1>
      </div>
    </div>
    <div class="row" style="margin-top: 2rem;">
      <div class="col-md-4"></div>
      <div class="col-md-4">
        <p class="lead">
          به سامانه جامع اطلاعات شهرداری قمصر خوش آمدید. برای پیگیری کد پستی و آدرس پستی خود، روی پیگیری کد پستی کلیک
          کنید تا اطلاعات آدرس پستی شما در سامانه پست نمایش داده شود. در صورت وجود مشکل با مرکز شهرداری قمصر تماس
          بگیرید.
        </p>
        <div class="col-md-4"></div>
      </div>
    </div>
    <div class="row" style="margin-top: 7rem;">
      <div class="col-md-12">
        <button class="btn btn-primary"
          style="padding: 10px 50px; font-size: 20px; width: 300px; background-color: #D75D8E; border-color: #D75D8E;"
          @click="handleClick">پیگیری کد پستی</button>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: 'App',
  methods: {
    goToExternalSite() {
      let urlParams = new URLSearchParams(window.location.search);
      const code = (urlParams.get('code'));
      window.open("https://gnaf2.post.ir/pdf/postalcodes/plate/" + code, '_blank');
    }
  }
}
</script>
