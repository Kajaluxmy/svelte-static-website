<script>
  let name = $state('');
  let email = $state('');
  let message = $state('');
  let submitted = $state(false);

  function handleSubmit() {
    submitted = true;
  }
</script>

<section class="bg-slate-900 px-6 py-24 text-center text-white">
  <div class="mx-auto max-w-3xl">

    <p class="font-semibold text-blue-400">
      Contact Us
    </p>

    <h1 class="mt-3 text-4xl font-bold sm:text-5xl">
      Let's Talk About Your Project
    </h1>

    <p class="mt-6 text-slate-300">
      Have a question or an idea? We'd love to hear from you.
    </p>

  </div>
</section>

<section class="px-6 py-20">
  <div class="mx-auto grid max-w-7xl gap-12 md:grid-cols-2">

    <div>

      <p class="font-semibold text-blue-600">
        Get In Touch
      </p>

      <h2 class="mt-2 text-3xl font-bold text-slate-900">
        We'd Love To Hear From You
      </h2>

      <p class="mt-6 leading-8 text-slate-600">
        Whether you have a question, project idea or simply want to say hello,
        feel free to contact us.
      </p>

      <div class="mt-10 space-y-6">

        <!-- Email -->
        <div class="flex gap-4">
          <div class="text-2xl">
            📧
          </div>

          <div>
            <h3 class="font-semibold text-slate-900">
              Email
            </h3>

            <p class="mt-1 text-slate-600">
              hello@astraspacex.com
            </p>
          </div>
        </div>

        <div class="flex gap-4">
          <div class="text-2xl">
            📞
          </div>

          <div>
            <h3 class="font-semibold text-slate-900">
              Phone
            </h3>

            <p class="mt-1 text-slate-600">
              +94 77 123 4567
            </p>
          </div>
        </div>

        <div class="flex gap-4">
          <div class="text-2xl">
            📍
          </div>

          <div>
            <h3 class="font-semibold text-slate-900">
              Address
            </h3>

            <p class="mt-1 text-slate-600">
              Jaffna, Sri Lanka
            </p>
          </div>
        </div>

      </div>
    </div>

    <div class="rounded-2xl border border-slate-200 bg-white p-8 shadow-sm">

      {#if submitted}
        <div class="mb-6 rounded-lg bg-green-50 p-4 text-green-700">
          Thank you, {name}! Your message has been submitted.
        </div>
      {/if}

      <form
        onsubmit={(event) => {
          event.preventDefault();
          handleSubmit();
        }}
        class="space-y-6"
      >

        <div>
          <label
            for="name"
            class="block font-medium text-slate-700"
          >
            Name
          </label>

          <input
            id="name"
            type="text"
            bind:value={name}
            placeholder="Enter your name"
            required
            class="mt-2 w-full rounded-lg border border-slate-300 px-4 py-3 outline-none transition focus:border-blue-600 focus:ring-2 focus:ring-blue-100"
          />
        </div>

        <div>
          <label
            for="email"
            class="block font-medium text-slate-700"
          >
            Email
          </label>

          <input
            id="email"
            type="email"
            bind:value={email}
            placeholder="Enter your email"
            required
            class="mt-2 w-full rounded-lg border border-slate-300 px-4 py-3 outline-none transition focus:border-blue-600 focus:ring-2 focus:ring-blue-100"
          />
        </div>

        <div>
          <label
            for="message"
            class="block font-medium text-slate-700"
          >
            Message
          </label>

          <textarea
            id="message"
            bind:value={message}
            placeholder="Write your message..."
            rows="5"
            required
            class="mt-2 w-full rounded-lg border border-slate-300 px-4 py-3 outline-none transition focus:border-blue-600 focus:ring-2 focus:ring-blue-100"
          ></textarea>
        </div>

        <button
          type="submit"
          class="w-full rounded-lg bg-blue-600 px-6 py-3 font-semibold text-white transition hover:bg-blue-700"
        >
          Send Message
        </button>

      </form>
    </div>

  </div>
</section>