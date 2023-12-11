import type { NuxtLoadingIndicator } from '#build/components';
<template>
  <div>
    <NuxtLoadingIndicator :color="'red'" :duration="200" :throttle="0" />
    <!-- here -->
    <FmNavbar />
    <div class="container mx-auto p-4">
      <NuxtPage></NuxtPage>
    </div>
  </div>
</template>

