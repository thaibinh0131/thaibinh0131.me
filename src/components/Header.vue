<template>
  <header
    class="fixed top-0 inset-x-0 z-50 h-$header-height px-6 bg-white dark:bg-dark-800 !bg-opacity-80 backdrop-blur"
  >
    <div
      class="max-w-screen-lg mx-auto h-full flex justify-between items-center"
    >
      <router-link
        class="text-2xl font-bold select-none outline-none"
        to="/"
        focusable="false"
      >
        thaibinh0131
      </router-link>
      <nav class="nav">
        <a
          href="https://github.com/thaibinh0131"
          target="_blank"
          rel="noopener"
          title="GitHub"
        >
          <div i-uil-github-alt />
        </a>

        <ToggleTheme />
      </nav>
    </div>
  </header>
</template>

<style scoped>
.nav {
  display: flex;
  align-items: center;
  gap: 0.2rem;
}

.nav img {
  margin-bottom: 0;
}

.nav a {
  cursor: pointer;
  text-decoration: none;
  color: inherit;
  transition: opacity 0.2s ease;
  opacity: 0.7;
  outline: none;
  padding: 0.5rem;
}

.nav a:hover {
  opacity: 1;
  text-decoration-color: inherit;
}

.backdrop-blur {
  backdrop-filter: blur(8px);
}
</style>
