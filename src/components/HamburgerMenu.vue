<template>
    <div class="hamburger-menu">
        <button class="menu-btn"><span></span></button>
    </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'HamburgerMenu',
  props: ['isOpened'],
})
</script>
<style scoped>
.menu-btn {
    border: none;
    position: fixed;
    top: 1em;
    right: 1em;
    display: flex;
    height: 5em;
    width: 5em;
    justify-content: center;
    align-items: center;
    z-index: 90;
    background: linear-gradient(#f19aff, #66f6ff);
}
.menu-btn span,
.menu-btn span:before,
.menu-btn span:after {
    content: '';
    display: block;
    height: 3px;
    width: 25px;
    border-radius: 3px;
    background-color: #ffffff;
    position: absolute;
}
.menu-btn span:before {
    bottom: 8px;
}
.menu-btn span:after {
    top: 8px;
}

@media screen and (min-width: 600px) {
  div.hamburger-menu {
    display: none;
  }
}
</style>