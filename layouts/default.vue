<template>
  <div>
    <header class="shadow-slate-50 shadow-md bg-white">
      <nav
        class="flex flex-1 container mx-auto justify-between align-middle p-4"
      >
        <NuxtLink to="/" class="font-bold text-xl">FMStore</NuxtLink>
        <ul class="flex gap-4">
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="/about">About</NuxtLink></li>
          <li><NuxtLink to="/login">Login</NuxtLink></li>
          <li><NuxtLink to="/logout">Logout</NuxtLink></li>
        </ul>
      </nav>
    </header>
    <div class="container mx-auto p-4 bg-gray-50">
      <!-- page renderes here -->
      <slot></slot>
    </div>
  </div>
</template>

<script></script>

<style scoped>
.router-link-exact-active {
  color: red;
}
</style>
