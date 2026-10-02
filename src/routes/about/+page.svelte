<script>
  const values = [
    {
      icon: '💡',
      title: 'Innovation',
      description:
        'We continuously explore better ways to solve problems.'
    },
    {
      icon: '🤝',
      title: 'Teamwork',
      description:
        'We believe great results come from working together.'
    },
    {
      icon: '⭐',
      title: 'Quality',
      description:
        'We focus on creating reliable and maintainable solutions.'
    },
    {
      icon: '❤️',
      title: 'Customer Focus',
      description:
        'We design solutions around real customer needs.'
    }
  ];
</script>

<section class="bg-slate-900 px-6 py-24 text-center text-white">
  <div class="mx-auto max-w-3xl">

    <p class="font-semibold text-blue-400">
      About Us
    </p>

    <h1 class="mt-3 text-4xl font-bold sm:text-5xl">
      We Build With Purpose
    </h1>

    <p class="mt-6 leading-8 text-slate-300">
      AstraSpaceX is a digital solutions company focused on creating simple,
      useful and modern technology experiences.
    </p>

  </div>
</section>

<section class="px-6 py-20">
  <div
    class="mx-auto grid max-w-7xl gap-12 md:grid-cols-2 md:items-center"
  >

    <div>
      <p class="font-semibold text-blue-600">
        Who We Are
      </p>

      <h2 class="mt-2 text-3xl font-bold text-slate-900">
        Technology With A Human Touch
      </h2>

      <p class="mt-6 leading-8 text-slate-600">
        We are a team of developers, designers and technology enthusiasts
        passionate about building digital products that solve real problems.
      </p>

      <p class="mt-4 leading-8 text-slate-600">
        From websites to digital applications, our goal is to make technology
        accessible, reliable and easy to use.
      </p>
    </div>

    <div class="rounded-3xl bg-blue-50 p-10 text-center">
      <div class="text-8xl">
        🌎
      </div>

      <h3 class="mt-6 text-2xl font-bold text-slate-900">
        Creating A Better Digital Future
      </h3>
    </div>

  </div>
</section>

<section class="bg-slate-50 px-6 py-20">
  <div class="mx-auto max-w-7xl">

    <div class="grid gap-8 md:grid-cols-2">

      <!-- Mission -->
      <div class="rounded-2xl bg-white p-8 shadow-sm">
        <div class="text-4xl">
          🎯
        </div>

        <h2 class="mt-5 text-2xl font-bold text-slate-900">
          Our Mission
        </h2>

        <p class="mt-4 leading-7 text-slate-600">
          To create accessible and reliable digital solutions that help
          individuals and businesses achieve their goals.
        </p>
      </div>

      <div class="rounded-2xl bg-white p-8 shadow-sm">
        <div class="text-4xl">
          🔭
        </div>

        <h2 class="mt-5 text-2xl font-bold text-slate-900">
          Our Vision
        </h2>

        <p class="mt-4 leading-7 text-slate-600">
          To become a trusted technology partner known for innovation,
          quality and meaningful digital experiences.
        </p>
      </div>

    </div>
  </div>
</section>

<section class="px-6 py-20">
  <div class="mx-auto max-w-7xl">

    <div class="text-center">
      <p class="font-semibold text-blue-600">
        Our Values
      </p>

      <h2 class="mt-2 text-3xl font-bold text-slate-900">
        What We Believe In
      </h2>
    </div>

    <div class="mt-12 grid gap-6 sm:grid-cols-2 lg:grid-cols-4">

      {#each values as value}
        <div class="rounded-2xl border border-slate-200 p-6 text-center">

          <div class="text-4xl">
            {value.icon}
          </div>

          <h3 class="mt-4 text-xl font-bold text-slate-900">
            {value.title}
          </h3>

          <p class="mt-3 leading-7 text-slate-600">
            {value.description}
          </p>

        </div>
      {/each}

    </div>
  </div>
</section>