<script setup>
  import { ref } from 'vue'

  const message = ref('سلام! به وب‌سایت من خوش آمدید.')
  function showMessage() {
   message.value = 'به‌زودی نمونه‌کارهای من را اینجا می‌بینی!'
  }
  import { RouterLink, RouterView } from 'vue-router'
  import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <h1>وب‌سایت شخصی من</h1>

    <nav>
      <a href="#">صفحه اصلی</a>
      <a href="#">درباره من</a>
      <a href="#">مهارت‌ها</a>
      <a href="#">نمونه‌کارها</a>
      <a href="#">ارتباط با من</a>
    </nav>
  </header>

  <section class="hero">
    <h2>سلام، من زینب هستم</h2>
    <p>به وب‌سایت شخصی من خوش آمدید.</p>
    <button @click="showMessage">
     مشاهده نمونه‌کارها
    </button>
    <p>{{ message }}</p>
  </section>

  <RouterView />
</template>

<style scoped>

header {
  background-color: #172554;
  color: white;
  padding: 25px;
  text-align: center;
}

nav {
  margin-top: 20px;
}

nav a {
  color: white;
  text-decoration: none;
  margin: 0 12px;
}
.hero {
  text-align: center;
  padding: 100px 20px;
  background-color: #f1f5f9;
  color: #172554;
}

.hero h2 {
  font-size: 36px;
  margin-bottom: 15px;
}

.hero p {
  font-size: 18px;
  margin-bottom: 25px;
}

.hero button {
  background-color: #2563eb;
  color: white;
  border: none;
  padding: 12px 25px;
  border-radius: 8px;
  cursor: pointer;
}
</style>
