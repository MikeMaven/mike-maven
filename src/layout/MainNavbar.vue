<template>
  <navbar
    position="fixed"
    type="primary"
    :transparent="transparent"
    :color-on-scroll="colorOnScroll"
    menu-classes="ml-auto"
  >
    <template slot-scope="{ toggle, isToggled }">
      <router-link v-popover:popover1 class="navbar-brand" to="/">
        Mike Maven
      </router-link>
      <el-popover
        ref="popover1"
        popper-class="popover"
        placement="bottom"
        width="200"
        trigger="hover"
      >
        <div class="popover-body">
          Expert Full Stack Web Developer &
          Unity3D Developer
        </div>
      </el-popover>
    </template>
    <template slot="navbar-menu">
      <li class="nav-item">
        <a
          class="nav-link"
          href="mailto:mikemaven@gmail.com?subject=Tell%20me%20more."
          target="_blank"
        >
          <i class="now-ui-icons tech_laptop"></i>
          <p>Contact</p>
        </a>
      </li>
      <drop-down
        tag="li"
        title="Web Development"
        icon="now-ui-icons objects_globe"
        class="nav-item"
      >
        <a 
          href="https://github.com/mikemaven"
          target="_blank"
          class="dropdown-item"
        >
          <i class="now-ui-icons business_chart-pie-36"></i> GitHub
        </a>
        <a
          href="https://demos.creative-tim.com/vue-now-ui-kit/documentation"
          target="_blank"
          class="dropdown-item"
        >
          <i class="now-ui-icons design_bullet-list-67"></i> Resume
        </a>
      </drop-down>
      <drop-down
              tag="li"
              title="Game Development"
              icon="now-ui-icons tech_controller-modern"
              class="nav-item"
      >
        <nav-link to="/landing">
          <i class="now-ui-icons location_compass-05"></i> A Dog's Dream
        </nav-link>
        <nav-link to="/login">
          <i class="now-ui-icons users_circle-08"></i> Login
        </nav-link>
        <nav-link to="/profile">
          <i class="now-ui-icons users_single-02"></i> Profile
        </nav-link>
      </drop-down>

      <li class="nav-item">
        <a
          class="nav-link"
          rel="tooltip"
          title="Follow Mike on Twitter"
          data-placement="bottom"
          href="https://twitter.com/FurlingForests"
          target="_blank"
        >
          <i class="fab fa-twitter"></i>
          <p class="d-lg-none d-xl-none">Twitter</p>
        </a>
      </li>
      <li class="nav-item">
        <a
          class="nav-link"
          rel="tooltip"
          title="Like A Dog's Dream on Facebook"
          data-placement="bottom"
          href="https://www.facebook.com/adogsdreamgame"
          target="_blank"
        >
          <i class="fab fa-facebook-square"></i>
          <p class="d-lg-none d-xl-none">Facebook</p>
        </a>
      </li>
      <li class="nav-item">
        <a
          class="nav-link"
          rel="tooltip"
          title="Follow us on Instagram"
          data-placement="bottom"
          href="https://www.instagram.com/adogsdreamgame"
          target="_blank"
        >
          <i class="fab fa-instagram"></i>
          <p class="d-lg-none d-xl-none">Instagram</p>
        </a>
      </li>
    </template>
  </navbar>
</template>

<script>
import { DropDown, NavbarToggleButton, Navbar, NavLink } from '@/components';
import { Popover } from 'element-ui';
export default {
  name: 'main-navbar',
  props: {
    transparent: Boolean,
    colorOnScroll: Number
  },
  components: {
    DropDown,
    Navbar,
    NavbarToggleButton,
    NavLink,
    [Popover.name]: Popover
  }
};
</script>

<style scoped></style>
