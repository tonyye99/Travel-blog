<template>
  <div class="flex-col min-h-screen">
    <Nav></Nav>
    <main class="flex-grow">
      <transition name="home">
        <Nuxt />
      </transition>
    </main>
    <Footer></Footer>
  </div>
</template>

<script>
import Nav from '@/components/nav'
import Footer from '@/components/footer'
export default {
  // eslint-disable-next-line vue/no-unused-components
  components: { Nav, Footer },
}
</script>

<style>
.home-enter-active,
.home-leave-active {
  transition: opacity 1s;
}
.home-enter,
.home-leave-active {
  opacity: 0;
}
</style>
