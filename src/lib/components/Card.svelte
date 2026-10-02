<script>
  let { title, description, icon } = $props();
</script>

<div
  class="group rounded-3xl border border-slate-200 bg-white/85 p-6 shadow-[0_10px_30px_rgba(15,23,42,0.05)] backdrop-blur-sm transition duration-300 hover:-translate-y-1 hover:border-blue-200 hover:shadow-[0_18px_40px_rgba(37,99,235,0.12)]"
>
  <div class="mb-5 inline-flex h-14 w-14 items-center justify-center rounded-2xl bg-blue-100 text-3xl shadow-inner shadow-blue-200/60">
    {icon}
  </div>

  <h3 class="text-xl font-bold text-slate-900">
    {title}
  </h3>

  <p class="mt-3 leading-7 text-slate-600">
    {description}
  </p>
</div>