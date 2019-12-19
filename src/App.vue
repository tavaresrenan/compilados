<template>
  <div id="app" class="st-container st-effect" v-bind:class="{ 'st-menu-open' : isOpen}">
      <app-NavMenu></app-NavMenu>
      <div class="st-pusher">
        <div class="st-content">
          <div class="st-content-inner">
            <img alt="Vue logo" src="./assets/logo.png" @click.prevent="openMenu">
          </div>
        </div>
      </div>
  </div>
</template>

<script>
import NavMenu from './components/NavMenu'

export default {
  name: 'app',
  components: {
    'app-NavMenu' : NavMenu
  },
  data () {
    return {
      isOpen : false
    }
  },
  methods: {
    openMenu() {
      this.isOpen = !this.isOpen;
    }
  }
}
</script>