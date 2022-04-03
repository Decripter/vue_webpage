<template>
<div :class="[theme_is_dark ? 'modal-background has-text-white' : '' ]">
<NavBar @on_change_theme="toggle_theme" />
<Contents/>
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