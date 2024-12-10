<script lang="ts">
  import { fly } from 'svelte/transition';
  import { page } from '$app/stores';
  import logo from '$lib/images/svelte-logo.svg';
  import github from '$lib/images/github.svg';

  let isMobileMenuOpen = false;
  let lastScrollY = 0;

  function handleScroll() {
    const currentScrollY = window.pageYOffset || document.documentElement.scrollTop;
    const header = document.querySelector('.header') as HTMLElement | null;

    if (header) {
      if (currentScrollY > lastScrollY) {
        // Scrolling down
        header.style.transform = 'translateY(-100%)';
      } else {
        // Scrolling up
        header.style.transform = 'translateY(0)';
      }
    }

    lastScrollY = currentScrollY;
    // Consider adding a throttle or debounce to prevent excessive function calls
  }
</script>

<svelte:window on:scroll={handleScroll} />

<header class="header">
  <div class="logo">
    <img src="/Remove-bg.ai_1732487706401.png" alt="SvelteKit" class="w-[2em] h-[2em]" />
  </div>

  <nav class="nav">
    <a href="/" class:active={$page.url.pathname === '/'}>Home</a>
    <a href="/about" class:active={$page.url.pathname === '/about'}>About</a>
    <a href="/chapters" class:active={$page.url.pathname === '/chapters'}>Videos</a>
    <a href="/resources" class:active={$page.url.pathname === '/resources'}>Books</a>
    <a href="/contact" class:active={$page.url.pathname === '/contact'}>Contact</a>
  </nav>

  <div class="search">
    <input type="text" placeholder="Search..." />
  </div>

  <!-- Mobile Menu Toggle -->
  <button class="menu-toggle" on:click={() => isMobileMenuOpen = !isMobileMenuOpen}>
    <svg viewBox="0 0 24 24" width="24" height="24">
      <path d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z" />
    </svg>
  </button>

  <!-- Mobile Menu -->
  <div class="mobile-menu" class:open={isMobileMenuOpen}>
    <a href="/">Home</a>
    <a href="/about">About</a>
    <a href="/chapters">Videos</a>
    <a href="/resources">Books</a>
    <a href="/contact">Contact</a>
  </div>
</header>

<style>
  .header {
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    width: 100%;
    background-color: #333;
    color: white;
    transition: transform 0.3s ease-in-out;
    z-index: 999;
  }

  .header.hide {
    transform: translateY(-100%);
  }

  .logo a {
    font-family: 'Great Vibes', cursive;
    font-size: 2rem;
    color: white;
    text-decoration: none;
  }

  .nav a {
    margin-left: 1rem;
    color: white;
    text-decoration: none;
    font-family: 'Roboto', sans-serif;
  }

  .nav a:hover, .nav a.active {
    text-decoration: underline;
  }

  .search input {
    padding: 0.5rem;
    border: none;
    border-radius: 4px;
  }

  .menu-toggle {
    display: none;
    background: none;
    border: none;
    color: white;
    cursor: pointer;
  }

  .mobile-menu {
    display: none;
    position: absolute;
    top: 100%;
    right: 0;
    background-color: #333;
    padding: 1rem;
    border-radius: 4px;
  }

  .mobile-menu.open {
    display: block;
  }

  @media (max-width: 768px) {
    .nav {
      display: none;
    }

    .menu-toggle {
      display: block;
    }
  }
</style>