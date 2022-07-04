<template>
  <nav>
    <ul>
      <li>
        <nuxt-link exact to="/">
          <AppLogo />
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/restaurants">Restaurants</nuxt-link>
      </li>
    </ul>
    <nuxt-link to="/cart">Cart <span class="smallnum">{{ cartCount }}</span></nuxt-link>
  </nav>
</template>

<script>
import AppLogo from '@/components/AppLogo.vue';
import { mapState, mapGetters } from 'vuex';
export default {
  computed: {
    ...mapState([
      'cart',
    ]),
    ...mapGetters([
      'cartCount',
    ]),
  },
  components: {
    AppLogo
  },
};
</script>

<style lang="scss" scoped>
</style>
