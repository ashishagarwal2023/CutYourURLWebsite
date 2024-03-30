<script>
  let activeQuestion = 0;

  const faqData = [
    {
      question: "What's CutYourURL?",
      answer:
        "CutYourURL is a advanced but free, open-source URL shortener. It allows you to shorten long URLs and make them easier to share. We have a dedicated about page for this question, you can check it out.",
    },
    {
      question: "I found a bug or have a idea",
      answer:
        "If you think we have a bug somewhere, go to our github repository and make a new issue so we can look into it.",
    },
    {
      question: "How can I contribute?",
      answer:
        "We have a issue as plans on github for the next features we want to implement. You can check it out and make a pull request if you want to help us. Any help is appreciated, like bug fixes or even reporting bugs.",
    },
    {
      question: "How can I contact you?",
      answer:
        "We have a seperate page on the website for contacting, thanks if you would like to have any support.",
    },
  ];
</script>

<svelte:head>
  <title>CutYourURL - FAQ</title>
</svelte:head>

<main class="flex flex-col flex-1 p-4">
  <section
    class="flex flex-col lg:flex-row justify-center items-center gap-6 lg:gap-10 py-20 lg:py-32 text-white text-left"
    id="faq"
  >
    <div
      class="flex flex-col lg:justify-center text-left gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="text-3xl sm:text-4xl md:text-5xl font-bold">
        Questions about <span class="poppins theme-400">CutYourURL</span>?
      </h2>
      <div class="mt-0">
        <article class="max-w-xl mx-auto">
          <div class="accordion">
            {#each faqData as item, index}
              <div class="accordion-item">
                <div
                  class="accordion-title"
                  on:click={() => (activeQuestion = index)}
                >
                  <h3 class="text-lg font-semibold">{item.question}</h3>
                  <i
                    class={activeQuestion === index
                      ? "fas fa-chevron-up"
                      : "fas fa-chevron-down"}
                  ></i>
                </div>
                <div
                  class="accordion-content {activeQuestion === index
                    ? 'show'
                    : ''}"
                >
                  <p class="text-base max-w-xl">{item.answer}</p>
                </div>
              </div>
            {/each}
          </div>
        </article>
      </div>
    </div>
  </section>
</main>
