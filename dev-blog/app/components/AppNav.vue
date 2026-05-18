<template>
    <nav>
        <NuxtLink
        to="/"
        :class="{ active: route.path === '/' }"
        >
      Hjem
    </NuxtLink>

        <NuxtLink
        to="/about"
        :class="{ active: route.path === '/about' }"
        >
      About
    </NuxtLink>
    
        <NuxtLink
        to="/contacts"
        :class="{ active: route.path === '/contacts'}"
        >
      Kontakter
    </NuxtLink>
  </nav>
</template>

<script setup>

const route = useRoute()

</script>

<style scoped>

    nav {
    display: flex;
    gap: 1rem;
}

    .active {
    font-weight: bold;
    color: red;
}

</style>