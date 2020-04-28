<template>
  <div>
    <div class="page-header clear-filter" filter-color="orange">
      <parallax
        class="page-header-image"
        style="background-image:url('img/dogsdreamenv.png')"
      >
      </parallax>
      <div class="container">
        <div class="content-center brand">
          <h1 class="h1-seo">A Dog's Dream</h1>
          <h3>An original Action/Adventure RPG by Mike Maven</h3>
        </div>
      </div>
    </div>
    <div class="main">
      <div class="section section-images">
        <div class="container">
          <div class="row">
            <div class="col-md-12">
              <div class="hero-images-container-3">
                <img src="img/sammyandneuro.png" alt="" />
              </div>
              <div class="hero-images-container-2">
                <img src="img/steam.png" alt="" />
                <h6 class="text-center">Wishlist on Steam</h6>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <signup-form></signup-form>
    <div class="section">
      <div class="container text-center">
        <div class="row justify-content-md-center">
          <div class="col-md-12 col-lg-8">
            <h2 class="title">Have you ever had a dream you couldn't wake up from?</h2>
            <h5 class="description">
              Sammy is just a Boston Terrier trying to make his way in a busy world, sleep deprived and overworked,  
              usure of himself and trapped in the daily grind, like so many of us. But the world that reveals itself to 
              him when he finds himself washed up on the shores of his sleeping mind is one that only he can save, in a 
              daring escape from a dreamworld being taken over by his fears and doubts.
            </h5>
            <h5 class="description">
              When Sammy is "woken up" by his own subconscious, an energy field who calls himself <i>Neuro</i>, he discovers a world 
              filled with memories of friends, both current and past, and ends up on mission to discover the keys that unlock his waking mind, 
              discovering friendship, facing his fears, and ultimately believing in himself.
            </h5>
            <h5 class="description">
              Guide Sammy and Neuro across 3 incredible "mini open worlds," interact with a hilarious cast of NPCs, participate in 
              fun mini games to build up skill, and take down the fears, doubts, and regrets threatening to destroy all the positive 
              memories that make up his inner life.
            </h5>
          </div>
        </div>
      </div>
    </div>
    <download-section></download-section>
  </div>
</template>
<script>
import { Parallax } from '@/components';
import SignupForm from './components/SignupForm';
import ExamplesSection from './components/ExamplesSection';
import DownloadSection from './components/DownloadSection';

export default {
  name: 'index',
  bodyClass: 'index-page',
  components: {
    Parallax,
    SignupForm,
    ExamplesSection,
    DownloadSection
  }
};
</script>
<style></style>
