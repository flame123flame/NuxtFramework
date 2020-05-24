<template>
  <div>
    <b-navbar type="dark" variant="dark">
      <b-navbar-nav>
        <b-nav-item v-b-toggle.sidebar-footer>MENU</b-nav-item>
      </b-navbar-nav>
    </b-navbar>
    <b-sidebar id="sidebar-footer" bg-variant="dark" aria-label="Sidebar with custom footer" no-header shadow     
      backdrop>
      <template v-slot:footer="{ hide }">
        <div class="d-flex bg-dark text-light align-items-center px-3 py-2">
          <strong class="mr-auto">Footer</strong>
          <b-button size="sm" @click="hide">Close</b-button>
        </div>
      </template>
      <div class="px-3 py-2"></div>
    </b-sidebar>
    <nuxt />
  </div>
</template>
<script>
import Vue from "vue";
import {
  BootstrapVue,
  BIcon,
  BIconArrowUp,
  BIconArrowDown
} from "bootstrap-vue";
Vue.use(BootstrapVue);
Vue.component("BIcon", BIcon);
Vue.component("BIconArrowUp", BIconArrowUp);
Vue.component("BIconArrowDown", BIconArrowDown);
export default {
  components: {
    BIcon,
    BIconArrowUp,
    BIconArrowDown
  }
};
</script>
<style scoped>
#test {
  color: #fff;
}
</style>