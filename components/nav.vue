<template>
  <nav
    class="
      transition-all
      duration-300
      bg-transparent
      absolute
      lg:fixed
      z-10
      pt-8
      lg:pt-5
      pb-8
      top-0
      left-0
      right-0
      px-5
      md:px-14
      py-5
    "
    :class="{ bgColor: addBgColour }"
  >
    <div class="grid grid-cols-2 text-white items-center justify-center">
      <div class="font-bold text-base">
        <h1>Travel with me</h1>
      </div>
      <div
        class="
          lg:hidden
          fixed
          top-4
          right-4
          rounded-full
          backdrop-filter backdrop-blur-lg
          w-14
          h-14
          flex
          items-center
          justify-center
          px-5
          py-5
          cursor-pointer
          z-30
        "
        @click="toggleMovileNav()"
      >
        <!-- Mobile menu button-->
        <div class="block cursor-pointer" :class="{ active: isMobileNavShow }">
          <span
            class="
              block
              w-6
              h-0.5
              m-1
              transition-all
              duration-300
              ease-in-out
              bg-black
            "
            :class="{ ['transform translate-y-1.5 rotate-45']: isMobileNavShow }"
          ></span>
          <span
            class="
              block
              w-6
              h-0.5
              m-1
              transition-all
              duration-300
              ease-in-out
              bg-black
            "
            :class="{ ['opacity-0']: isMobileNavShow }"
          ></span>
          <span
            class="
              block
              w-6
              h-0.5
              m-1
              transition-all
              duration-300
              ease-in-out
              bg-black
            "
            :class="{
              ['transform -translate-y-1.5 -rotate-45']: isMobileNavShow,
            }"
          ></span>
        </div>
        <!-- </button> -->
      </div>
      <div class="hidden lg:flex items-center justify-self-end space-x-5">
        <NuxtLink
          href="#"
          to="/"
          class="hover:text-green-600 px-3 py-2 rounded-md font-medium"
          >Blogs</NuxtLink
        >

        <NuxtLink
          href="#"
          to="about"
          exact-active-class="text-green-400 dark:text-green-500"
          class="hover:text-green-600 px-3 py-2 rounded-md font-medium"
          >About</NuxtLink
        >
      </div>
    </div>
    <!-- Mobile menu, show/hide based on menu state. -->
    <div
      class="
        transition-all
        duration-500
        overflow-scroll
        fixed
        w-full
        h-screen
        top-0
        left-0
        flex
        items-center
        justify-center
        bg-white
      "
      :class="{
        [`opacity-100 overflow-hidden z-20`]: isMobileNavShow,
        [`opacity-0 overflow-hidden hidden`]: !isMobileNavShow,
      }"
    >
      <NuxtLink
        href="#"
        to="about"
        exact-active-class="text-green-400 dark:text-green-500"
        class="hover:text-green-600 px-3 py-2 rounded-md font-medium"
        >About</NuxtLink
      >
    </div>
  </nav>
</template>
<script>
export default {
  data() {
    return {
      addBgColour: false,
      isMobileNavShow: false,
    }
  },
  mounted() {
    window.addEventListener('scroll', this.onScroll, true)
  },
  methods: {
    onScroll(e) {
      const scroll = window.scrollY
      if (scroll < 0) {
        return
      }
      if (
        /Android|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(
          navigator.userAgent
        )
      ) {
        return
      }
      this.addBgColour = scroll > 100
    },
    toggleMovileNav() {
      this.isMobileNavShow = !this.isMobileNavShow
    },
  },
}
</script>
<style scoped>
.bgColor {
  background-color: #1a759f;
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
}

/* .hamburger {
  display: block;
  cursor: pointer;
} */

/* .bar {
  display: block;
  width: 25px;
  height: 3px;
  margin: 5px auto;
  -webkit-transition: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
  background-color: #101010;
}

.hamburger.active .bar:nth-child(2) {
  opacity: 0;
}

.hamburger.active .bar:nth-child(1) {
  transform: translateY(8px) rotate(45deg);
}

.hamburger.active .bar:nth-child(3) {
  transform: translateY(-8px) rotate(-45deg);
} */

/* .mobile-menu {
  transition: 0.5s all ease-out;
  overflow: scroll;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  align-items: center;
  justify-content: center;
}

.show {
  opacity: 1;
  overflow: hidden;
  z-index: 20;
}

.hide {
  opacity: 0;
  overflow: hidden;
  display: none;
} */

/* @media screen and (max-width: 768px) {
  nav {
    position: absolute;
    z-index: 905;
  }
  .mobile-nav {
    position: fixed;
    top: 2.5%;
    right: 5%;
    border-radius: 100px;
    backdrop-filter: blur(2em);
    width: 58px;
    height: 58px;
    align-items: center;
    display: flex;
    z-index: 903;
    justify-content: center;
  }
} */
</style>
