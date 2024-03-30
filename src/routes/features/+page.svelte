<script>
  let features = [
    {
      name: "Custom Short Links",
      icon: "fa-solid fa-link",
      description: "Generate custom ID in shorts so it appears cool",
    },
    {
      name: "reCAPTCHA",
      icon: "fa-solid fa-shield",
      description:
        "Protect your links with reCAPTCHA to prevent spam and abuse",
    },
    {
      name: "Visibility and Tracking",
      icon: "fa-solid fa-eye",
      description:
        "Have some free visitors when your link is public and visible on the main page",
    },
    {
      name: "QR Codes",
      icon: "fa-solid fa-qrcode",
      description: "Automatically-generated QR codes for every of your links",
    },
    {
      name: "Expiry",
      icon: "fa-solid fa-trash",
      description:
        "Are your links important to you? Choose to delete them automatically at specific clicks or time!",
    },
    {
      name: "Accounts",
      icon: "fa-solid fa-user",
      description:
        "Accounts that provide you with more features and control over your links",
    },
    {
      name: "Recents Generated",
      icon: "fa-solid fa-clock-rotate-left",
      description:
        "View the most recent generated links by the community or hide yours by making it private",
    },
    {
      name: "Unlimited",
      icon: "fa-solid fa-border-all",
      description:
        "Everything we've provided is unlimited. No limits, no restrictions, no hidden fees and for free.",
    },
    {
      name: "Coming soon",
      icon: "fa-solid fa-ellipsis",
      description:
        "Very soon we would have a dashboard, API, browser extension, and a lot more we don't know",
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section id="features" class="py-20 slg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        Why are we <span class="highlight">better</span>?
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        The <span class="poppins theme-400">Features</span> of CutYourURL
      </h3>
    </div>
    <a
      href="#"
      target="_blank"
      class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-theme-700 hover:bg-400 hover:text-white duration-200"
    >
      <i class="fa-regular fa-circle-play" />
      <p>Watch the video</p>
    </a>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 sm:gap-8">
      {#each features as feature}
        <div
          class="p-4 sm:p-6 md:p-8 flex flex-col gap-4 rounded-lg border border-solid border-theme-700 text-center cursor-pointer group hover:border-theme-400 duration-200"
        >
          <div
            class="free grid place-items-center px-4 text-5xl md:text-6xl -mt-10 sm:-mt-12 md:-mt-14 lg:-mt-16 mx-auto duration-200"
          >
            <i class={feature.icon + " theme-400 text-5xl py-1 bg-slate-950"} />
            <h3 class="font-medium text-xl sm:text-2xl md:text-3xl">
              {feature.name}
            </h3>
          </div>
          {feature.description}
        </div>
      {/each}
    </div>
    <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl text-center">
      It's not
      <span class="highlight">just that!</span><br />
      <span class="text-2xl sm:text-3xl md:text-4xl text-center">
        More things are <span class="highlight">coming</span>!
      </span>
    </h3>
  </section>
</main>
