<template>
  <div id="app" class="nav-menu-container nav-menu-effect" 
        v-bind:class="{ 'nav-menu-menu-open' : isOpen }" >
      <app-NavMenu></app-NavMenu>
      <div class="nav-menu-pusher">
        <div class="nav-menu-content">
          <div class="nav-menu-content-inner">
            <img alt="Vue logo" src="./assets/logo.png"
            style="width: 3.5em" @click.prevent="openMenu">
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