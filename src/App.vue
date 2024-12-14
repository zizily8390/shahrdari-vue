<template>
  <div class="container text-center">
    <div class="row" style="margin-top: 1rem; margin-bottom: 1rem;"></div>
    <div class="row">
      <div class="col-md-12 mb-1">
        <h1 style="font-family: Tahrir;margin-bottom: 2rem;">خوش آمدید</h1>
        <img src="/public/assets/images/pez.jpg" alt="">
      </div>
    </div>
    <div class="row" style="margin-top: 7rem;">
      <div class="col-md-4"></div>
      <div class="col-md-4">
        <p class="lead">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos, inventore quo. Ad dolorum quo tenetur cum
          suscipit blanditiis modi autem sequi quas ipsum libero consequatur, nihil neque voluptatum hic natus!
        </p>
        <div class="col-md-4"></div>
      </div>
    </div>
    <div class="row" style="margin-top: 11rem;">
      <div class="col-md-12">
        <button class="btn btn-primary" style="padding: 10px 50px; font-size: 20px; width: 300px;"
          @click="handleClick">کلیک
          کنید</button>
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
