<template>
   <nav class="navbar" role="navigation" aria-label="main navigation">
            <div class="navbar-brand">
              <a class="navbar-item" >
                <img src="../assets/logo.png" width="30" height="28">
              </a>

              <a @click="toOpenMenu" role="button" class="navbar-burger" :class="[openMenu ? 'is-active' : '']" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
              </a>

            </div>
          
            <div id="navbarBasicExample" class="navbar-menu" :class="[openMenu ? 'is-active' : '']">
              <div class="navbar-start">
                <a class="navbar-item">
                  Home
                </a>
          
                <a class="navbar-item">
                  Documentation
                </a>
          
                <div class="navbar-item has-dropdown is-hoverable">
                  <a class="navbar-link">
                    More
                  </a>
          
                  <div class="navbar-dropdown">
                    <a class="navbar-item">
                      About
                    </a>
                    <a class="navbar-item">
                      Jobs
                    </a>
                    <a class="navbar-item">
                      Contact
                    </a>
                    <hr class="navbar-divider">
                    <a class="navbar-item">
                      Report an issue
                    </a>
                  </div>
                </div>
              </div>
              
              <div class="navbar-end">
                <div class="navbar-item">
                  <label  class="switch">
                  <input @click="dark_mode_toggle" type="checkbox" v-bind:checked="theme_dark[0]">
                  <span class="slider round" ></span>
                </label>
              </div>
                <div class="navbar-item">
                  <div class="buttons">
                    <a class="button is-primary">
                      <strong>Sign up</strong>
                    </a>
                    <a class="button is-light">
                      Log in
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </nav>
</template>

<script>
export default {
  name: 'NavBar',
  props:["theme_dark"],
  data(){
    return {
      openMenu: false

    }
  },
  

  methods:{
    
    dark_mode_toggle(){
     this.$emit('on_change_theme')
     if(this.openMenu){
       this.openMenu = false
     }
    },
    toOpenMenu(){
      this.openMenu=!this.openMenu

    }
  },
  
  
  
}
</script>
<style lang="css">

      .switch {
        position: relative;
        display: inline-block;
        width: 38px;
        height: 18px;
      }
      
      .switch input { 
        opacity: 0;
        width: 0;
        height: 0;
      }
      
      .slider {
        position: absolute;
        cursor: pointer;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: #ccc;
        -webkit-transition: .4s;
        transition: .4s;
      }
      
      .slider:before {
        position: absolute;
        content: "";
        height: 14px;
        width: 14px;
        left: 4px;
        bottom: 2px;
        background-color: white;
        -webkit-transition: .4s;
        transition: .4s;
      }
      
      input:checked + .slider {
        background-color: #2196F3;
      }
      
      input:focus + .slider {
        box-shadow: 0 0 1px #2196F3;
      }
      
      input:checked + .slider:before {
        -webkit-transform: translateX(18px);
        -ms-transform: translateX(18px);
        transform: translateX(18px);
      }
      
      /* Rounded sliders */
      .slider.round {
        border-radius: 34px;
      }
      
      .slider.round:before {
        border-radius: 50%;
      }
</style>
