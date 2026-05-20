<template>
  <div>
    <header>
      <nav>
        <NuxtLink to="/">Dev Blog</NuxtLink>
        <NuxtLink to="/blog">Blogg</NuxtLink>
        <NuxtLink to="/about">Om</NuxtLink>
      </nav>
    </header>
    <main>
      <slot />
    </main>
    <footer>
      <p>Dev Blog &copy; 2026</p>
    </footer>
  </div>
</template>

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