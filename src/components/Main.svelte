<script>
  let slideshow = [
    {
      name: "CutYourURL Main Page (Guest)",
      src: "./images/show.png",
    },
    {
      name: "CutYourURL Logged (Home) Page: With Advanced Options",
      src: "./images/main-logged.png",
    },
    {
      name: "CutYourURL Account Page",
      src: "./images/account.png",
    },
    {
      name: "CutYourURL Short Page: with views and QR code",
      src: "./images/short.png",
    },
    {
      name: "CutYourURL Login Page",
      src: "./images/login.png",
    },
    {
      name: "CutYourURL Signup Page",
      src: "./images/signup.png",
    },
  ];

  let features = [
    {
      name: "Custom Short Links",
      icon: "fa-solid fa-link",
      description: "Generate custom short links to not be unknown!",
    },
    {
      name: "reCAPTCHA",
      icon: "fa-solid fa-shield",
      description:
        "Protect your links with reCAPTCHA to prevent spam and abuse.",
    },
    {
      name: "Visibility and Tracking",
      icon: "fa-solid fa-eye",
      description:
        "Make your link public and get it listed in the recent ones, or choose private. Track your visitors and not get lost!",
    },
    {
      name: "QR Codes",
      icon: "fa-solid fa-qrcode",
      description:
        "Short Links too short? We've got QR codes for every of you!",
    },
    {
      name: "Expiry",
      icon: "fa-solid fa-trash",
      description:
        "Are your links important to you? Automatically delete them without worrying. At a specific time, or a limited clicks?",
    },
    {
      name: "Coming soon",
      icon: "fa-solid fa-ellipsis",
      description: "More features are coming soon! Stay tuned!",
    },
  ];
</script>

<svelte:head>
  <title>CutYourURL</title>
</svelte:head>

<main class="flex flex-col flex-1 p-4">
  <section
    id="home"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Meet <span class="poppins theme-400">CutYourURL </span><br />
        <span class="poppins theme-400">URL Shortener</span>
        <br /><span class="text-3xl sm:text-4xl md:text-5xl"
          ><span class="premium">Free. Open-source. Powerful</span>
        </span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        Fully-fledged <span class="theme-400 poppins">Bitly URL Shortener</span>
        Clone. Give it a try!
      </p>
      <a
        class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-all bg-white text-slate-950 cursor-pointer rounded-full"
        href="#"
        target="_blank"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-400 opacity-50 group-hover:translate-x-full z-0 duration-200"
        />
        <h4 class="relative z-9 arrow-button hover:theme-900">
          Try it out! <i class="fa-solid fa-arrow-right px-1"></i>
        </h4>
      </a>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <img
        src={"images/laptop.png"}
        alt="CutYourURL URL Shortener"
        class="object-cover z-[2] max-h-[70vh] rounded-lg"
        style="transform: scaleX(-1);"
      />
    </div>
  </section>
  <section id="features" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        Curious to <span class="poppins theme-400">know</span> more?
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
      Not enough?<br />
      View
      <a href="/features" class="theme-400 hover:theme-500 duration-100"
        >all features</a
      >!
    </h3>
  </section>
  <section
    id="compare"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
    <h5 class={"text-2xl sm:text-3xl font-semibold text-center poppins"}>
      It builds a <span class="theme-400">difference!</span>
    </h5>
    <div
      class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
    >
      <table class="bg-white text-slate-700 rounded text-center">
        <thead class={"border-b border-solid border-slate-200"}>
          <tr class="">
            <th />
            <th class="whitespace-nowrap p-2 px-4">Bitly</th>
            <th class="whitespace-nowrap p-2 px-4">TinyURL</th>
            <th class="whitespace-nowrap p-2 px-4">Rebrandly</th>
            <th class="bg-700 text-white whitespace-nowrap p-4 px-8"
              >CutYourURL</th
            >
          </tr>
        </thead>
        <tbody>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
              >Plan</td
            >
            <td>Free and Paid</td>
            <td>Free and Paid</td>
            <td>Free and Paid</td>
            <td class="text-green-500">Free</td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
              >Fast Redirects</td
            >
            <td>Only in Paid</td>
            <td>Not available</td>
            <td>Not available</td>
            <td class="text-green-500">All in Free</td>
          </tr>
          <tr>
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
              >Analytics</td
            >
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-green-500" /></td>
          </tr>
          <tr class="border-t border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
              >Choosen Expiry</td
            >
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-green-500" /></td>
          </tr>
        </tbody>
      </table>
    </div>
    <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl text-center">
      That's too few?<br />
      See the
      <a href="#" class="theme-400 hover:theme-500 duration-100"
        >comparing list</a
      >!
    </h3>
    <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
      <p>Scroll to see more &rarr;</p>
    </div>
  </section>
</main>
