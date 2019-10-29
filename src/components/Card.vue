<template>
  <div class="card">
    <picture class="card-image__wrapper card-image__wrapper--center-center">
      <img
        src="./../assets/hulk.jpg"
        :alt="alt">
    </picture>
    <div>
      <h3>Object fit polyfill for IE and iOS</h3>
    </div>
  </div>
</template>

<script>
import objectFitImages from 'object-fit-images';
export default {
  name: 'Card',
  props: {
    src: {
      type: String,
      default: ''
    },
  },
  mounted() {
    objectFitImages();
  }
}
</script>

<style>
  .card {
    width: 400px;
    height: auto;
  }
  .card-image__wrapper {
    position: relative;
    display: block;
    width: 100%;
    height: 0;
    padding-top: 100%;
  }
  .card-image__wrapper img{
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    object-fit: cover;
    object-position: left bottom;
  }
  .card-image__wrapper--left-bottom img {
    font-family: 'object-fit: cover; object-position: left bottom;';
  }
  .card-image__wrapper--right-bottom img {
    font-family: 'object-fit: cover; object-position: right bottom;';
  }
  .card-image__wrapper--center-bottom img {
    font-family: 'object-fit: cover; object-position: center bottom;';
  }
  .card-image__wrapper--right-top img {
    font-family: 'object-fit: cover; object-position: right top;';
  }
  .card-image__wrapper--left-top img {
    font-family: 'object-fit: cover; object-position: left top;';
  }
  .card-image__wrapper--center-top img {
    font-family: 'object-fit: cover; object-position: center top;';
  }
  .card-image__wrapper--center-center img {
    font-family: 'object-fit: cover; object-position: center center;';
  }
</style>
