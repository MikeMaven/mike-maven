<template>
  <div>
    <div class="page-header clear-filter" filter-color="orange">
      <parallax
        class="page-header-image"
        style="background-image:url('img/bg5.jpg')"
      >
      </parallax>
      <div class="container">
        <div class="photo-container">
          <img src="img/mike.jpg" alt="" />
        </div>
        <h3 class="title">Mike Maven</h3>
        <p class="category">Developer</p>
      </div>
    </div>
    <div class="section">
      <div class="container">
        <div class="button-container">
          <a href="https://www.facebook.com/adogsdream" class="btn btn-primary btn-round btn-lg">Follow</a>
          <a
            href="https://www.twitter.com/FurlingForests"
            class="btn btn-default btn-round btn-lg btn-icon"
            rel="tooltip"
            title="Follow me on Twitter"
          >
            <i class="fab fa-twitter"></i>
          </a>
          <a
            href="https://www.instagram.com/furling_forests/"
            class="btn btn-default btn-round btn-lg btn-icon"
            rel="tooltip"
            title="Follow me on Instagram"
          >
            <i class="fab fa-instagram"></i>
          </a>
        </div>
        <h3 class="title">About me</h3>
        <h5 class="description">
          A former touring musician, arcade bar owner, and entrepreneur, I am 
          a software engineer with a sense of purpose. With a background in video games, 
          a full-time gig in the healthcare industry, and a wide range of skills in my field 
          that range from game development to full stack web application development, 
          and cloud deployment to building native iOS and Android apps, I offer both the 
          passion of someone who appreciates and understands the business of your vision and 
          the technical proficiency to help you make it a reality. An experienced team manager, 
          I have been working with fellow bootcamp graduates since I first entered the industry, helping 
          develop protoypes and finished products on time and under budget.
        </h5>
      </div>
    </div>
  </div>
</template>
<script>
import { Tabs, TabPane } from '@/components';

export default {
  name: 'profile',
  bodyClass: 'profile-page',
  components: {
    Tabs,
    TabPane
  }
};
</script>
<style></style>
