<template>
  <footer
    class="footer"
    :class="{ [`footer-${type}`]: type }"
    :data-background-color="backgroundColor"
  >
    <div class="container">
      <nav>
        <ul>
          <li>
            <a href="https://www.mikemavendev.com">
              Mike Maven
            </a>
          </li>
          <li>
            <a href="https://www.facebook.com/adogsdreamgame">
              Facebook
            </a>
          </li>
          <li>
            <a href="https:///www.instagram.com/adogsdreamgame">
              Instagram
            </a>
          </li>
        </ul>
      </nav>
      <div class="copyright">
        &copy; {{ year }}, Designed by
        <a href="https:///www.invisionapp.com" target="_blank" rel="noopener"
          >Invision</a
        >. Coded by
        <a href="/" target="_blank" rel="noopener"
          >Mike Maven</a
        >.
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  props: {
    backgroundColor: String,
    type: String
  },
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>
<style></style>
