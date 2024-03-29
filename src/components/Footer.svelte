<script>
    let links = [
        { label: 'Home', url: '/' },
        { label: 'About', url: '/about' },
        // { label: 'Blog', url: '/blog' },
        { label: 'Features', url: '/features' },
        { label: 'FAQ', url: '/faq' },
        { label: 'Help', url: '/help' },
    ];

    let socials = [
        { label: 'GitHub', url: 'https://github.com/ashishagarwal2023/CutYourURL/', icon: 'fab fa-github', target: "_blank"},
        { label: 'Website', url: '#', icon: 'fas fa-globe', target: ""},
        { label: 'Email', url: 'mailto:code.with.aasheesh@gmail.com', icon: 'fas fa-envelope', target: "_blank"},
    ];

    let currentYear = new Date().getFullYear();
</script>

<section class="bg-black border-violet-400">
    <div class="max-w-screen-xl px-4 py-12 mx-auto space-y-8 overflow-hidden sm:px-6 lg:px-8">
        <nav class="flex flex-wrap justify-center -mx-5 -my-2">
            {#each links as link}
                <div class="px-3 py-2">
                    <a href={link.url} class="text-base leading-6 text-gray-200 hover:text-white duration-200">
                        {link.label}
                    </a>
                </div>
            {/each}
        </nav>
        <div class="flex justify-center mt-8 space-x-6">
            {#each socials as social}
                <a href={social.url} class="text-gray-400 py-4 hover:text-gray-100 duration-200" target="{social.target}">
                    <span class="sr-only">{social.label}</span>
                    <i class={social.icon}></i>
                </a>
            {/each}
        </div>
        <p class="mt-8 text-base leading-6 text-center text-gray-400">
            © {currentYear} CutYourURL, Inc. All rights reserved. 
            <br>CutYourURL is not affilated to anyone and is a open-source project.
        </p>
    </div>
</section>
