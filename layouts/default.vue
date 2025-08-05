<template>
  <div>
    <Header />
    <main>
      <transition name="fade" mode="out-in">
        <slot />
      </transition>
    </main>
    <Footer />
  </div>
</template>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s ease;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style>
