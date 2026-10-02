<script>
  import Card from '#lib/components/Card.svelte';

  let count = $state(0);

  const features = [
    {
      icon: '💻',
      title: 'Web Development',
      description:
        'We create modern, responsive and user-friendly websites using modern technologies.'
    },
    {
      icon: '🎨',
      title: 'UI Design',
      description:
        'Clean and intuitive interfaces designed to provide a great user experience.'
    },
    {
      icon: '⚡',
      title: 'Fast Performance',
      description:
        'Optimized websites that load quickly and work smoothly across devices.'
    },
    {
      icon: '🔒',
      title: 'Reliable Solutions',
      description:
        'Secure and reliable digital solutions built with quality and maintainability in mind.'
    }
  ];

  const badges = ['Brand strategy', 'UX design', 'Web development'];
</script>

<section class="relative overflow-hidden bg-gradient-to-br from-blue-50 via-white to-indigo-50">
  <div class="absolute inset-x-0 top-0 h-40 bg-[radial-gradient(circle_at_center,_rgba(96,165,250,0.18),_transparent_60%)]"></div>

  <div
    class="relative mx-auto grid min-h-[650px] max-w-7xl items-center gap-12 px-6 py-20 md:grid-cols-2"
  >
    <div>
      <div class="mb-6 flex flex-wrap gap-3">
        {#each badges as badge}
          <span class="rounded-full border border-blue-200 bg-white/80 px-3 py-1 text-xs font-semibold uppercase tracking-[0.18em] text-blue-700 shadow-sm">
            {badge}
          </span>
        {/each}
      </div>

      <p class="mb-4 font-semibold text-blue-600">
        Welcome to AstraSpaceX
      </p>

      <h1
        class="text-4xl font-black leading-tight tracking-tight text-slate-900 sm:text-5xl lg:text-6xl"
      >
        Building Digital Experiences That Matter
      </h1>

      <p class="mt-6 max-w-xl text-lg leading-8 text-slate-600">
        We create modern websites and digital solutions that help businesses
        grow and connect with their customers.
      </p>

      <div class="mt-8 flex flex-wrap gap-4">
        <a
          href="/contact"
          class="rounded-xl bg-blue-600 px-6 py-3 font-semibold text-white shadow-lg shadow-blue-600/20 transition hover:-translate-y-0.5 hover:bg-blue-700"
        >
          Get Started
        </a>

        <a
          href="/about"
          class="rounded-xl border border-slate-300 bg-white px-6 py-3 font-semibold text-slate-700 shadow-sm transition hover:-translate-y-0.5 hover:bg-slate-50"
        >
          Learn More
        </a>
      </div>

      <div class="mt-10 flex flex-wrap items-center gap-6 rounded-2xl border border-slate-200 bg-white/70 p-4 backdrop-blur-sm shadow-sm">
        <div>
          <p class="text-sm text-slate-500">Interested visitors</p>
          <div class="mt-1 flex items-center gap-3">
            <span class="text-2xl font-bold text-blue-600">{count}</span>
            <button
              onclick={() => count++}
              class="rounded-lg bg-slate-900 px-3 py-2 text-sm font-medium text-white transition hover:bg-slate-800"
            >
              + Interested
            </button>
          </div>
        </div>
      </div>
    </div>

    <div class="relative hidden md:block">
      <div class="absolute -left-8 top-10 h-32 w-32 rounded-full bg-cyan-300/50 blur-3xl"></div>
      <div class="absolute -right-4 bottom-8 h-32 w-32 rounded-full bg-indigo-300/40 blur-3xl"></div>

      <div class="relative overflow-hidden rounded-[2rem] border border-blue-200 bg-slate-900 p-8 text-white shadow-[0_30px_80px_rgba(15,23,42,0.22)]">
        <div class="flex items-center justify-between text-sm text-slate-300">
          <span>Launch dashboard</span>
          <span class="rounded-full bg-emerald-500/20 px-2 py-1 text-emerald-300">98.2%</span>
        </div>

        <div class="mt-8 text-5xl">🚀</div>

        <h2 class="mt-8 text-3xl font-bold">
          Turn Ideas Into Reality
        </h2>

        <p class="mt-4 leading-7 text-slate-300">
          We combine creativity, technology and strategy to create meaningful
          digital experiences.
        </p>

        <div class="mt-8 grid gap-4 sm:grid-cols-2">
          <div class="rounded-2xl bg-white/8 p-4 backdrop-blur-sm">
            <p class="text-xs uppercase tracking-[0.2em] text-slate-300">Speed</p>
            <p class="mt-2 text-2xl font-bold">2.4x</p>
          </div>
          <div class="rounded-2xl bg-white/8 p-4 backdrop-blur-sm">
            <p class="text-xs uppercase tracking-[0.2em] text-slate-300">Growth</p>
            <p class="mt-2 text-2xl font-bold">+124%</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="bg-white px-6 py-20">
  <div class="mx-auto max-w-7xl">
    <div class="mx-auto max-w-2xl text-center">
      <p class="font-semibold text-blue-600">What We Do</p>

      <h2 class="mt-2 text-3xl font-bold text-slate-900 sm:text-4xl">
        Our Services
      </h2>

      <p class="mt-4 leading-7 text-slate-600">
        We provide simple and effective digital solutions for modern
        businesses.
      </p>
    </div>

    <div class="mt-12 grid gap-6 sm:grid-cols-2 lg:grid-cols-4">
      {#each features as feature}
        <Card
          title={feature.title}
          description={feature.description}
          icon={feature.icon}
        />
      {/each}
    </div>
  </div>
</section>

<section class="bg-blue-600 px-6 py-20 text-center text-white">
  <div class="mx-auto max-w-3xl">
    <h2 class="text-3xl font-bold sm:text-4xl">Ready to Start Your Project?</h2>

    <p class="mt-4 text-blue-100">
      Let's create something amazing together.
    </p>

    <a
      href="/contact"
      class="mt-8 inline-block rounded-xl bg-white px-6 py-3 font-semibold text-blue-600 shadow-lg shadow-blue-900/10 transition hover:-translate-y-0.5 hover:bg-blue-50"
    >
      Contact Us
    </a>
  </div>
</section>