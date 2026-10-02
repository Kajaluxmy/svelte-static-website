<script>
  import { page } from '$app/state';

  let menuOpen = $state(false);

  const navigation = [
    { name: 'Home', href: '/' },
    { name: 'About', href: '/about' },
    { name: 'Contact', href: '/contact' }
  ];
</script>

<nav class="sticky top-0 z-50 border-b border-slate-200 bg-white/95 backdrop-blur">
  <div class="mx-auto flex max-w-7xl items-center justify-between px-6 py-4">

    <a href="/" class="text-2xl font-bold text-blue-600">
      AstraSpaceX
    </a>

    <div class="hidden items-center gap-8 md:flex">
      {#each navigation as item}
        <a
          href={item.href}
          class="text-slate-700 transition hover:text-blue-600"
          class:font-semibold={page.url.pathname === item.href}
          class:text-blue-600={page.url.pathname === item.href}
        >
          {item.name}
        </a>
      {/each}
    </div>

    <button
      class="rounded-lg p-2 text-2xl text-slate-700 md:hidden"
      onclick={() => (menuOpen = !menuOpen)}
      aria-label="Toggle navigation menu"
    >
      {#if menuOpen}
        ✕
      {:else}
        ☰
      {/if}
    </button>
  </div>

  {#if menuOpen}
    <div class="border-t border-slate-200 bg-white px-6 py-4 md:hidden">
      <div class="flex flex-col gap-4">
        {#each navigation as item}
          <a
            href={item.href}
            onclick={() => (menuOpen = false)}
            class="text-slate-700 hover:text-blue-600"
            class:font-semibold={page.url.pathname === item.href}
            class:text-blue-600={page.url.pathname === item.href}
          >
            {item.name}
          </a>
        {/each}
      </div>
    </div>
  {/if}
</nav>