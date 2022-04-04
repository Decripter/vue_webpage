<template>
<div :class="[theme_is_dark ? 'has-background-dark has-text-white' : '' ]" 
style="transition: background-color 500ms ease-out 5ms;height: 100vh;">
<NavBar @on_change_theme="toggle_theme" :theme_dark="[theme_is_dark ? true : false]"/>
<Contents :themeDark="[theme_is_dark ? true : false]"/>
</div>
</template>

<script>

import NavBar from '@/components/NavBar.vue'
import Contents from '@/components/Contents.vue'

export default {

  name: 'Home',

  components: {

    NavBar,
    Contents

  },
  data(){
    return{
      theme_is_dark: false
    }
  },
  methods:{
    toggle_theme(){
      this.theme_is_dark = !this.theme_is_dark
      console.log(this.theme_is_dark)
    }
  }

}

</script>