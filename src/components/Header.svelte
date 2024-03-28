<script>
	export let y;

	let tabs = [
		{ name: "About", link: "/about" },
		{ name: "Blog", link: "/blog" },
		{ name: "Features", link: "/features" },
		{ name: "FAQ", link: "/faq" },
		{ name: "Help", link: "/help" },
	];
</script>

<header
	class={"z-[99] sticky top-0 duration-200 px-6 flex items-center justify-between border border-solid select-none " +
		(0 > y
			? "py-10 bg-transparent border-transparent"
			: "py-3 bg-gray-900 border-transparent")}
>
	<h1 class="font-medium">
		<a href="/"><b class="font-bold poppins text-orange-400">CutYourURL</b> URL Shortener</a>
	</h1>
	<div class="sm:flex items-center ml-auto pr-4 gap-4 hidden">
		{#each tabs as tab, index}
			<a
				href={tab.link}
				class="duration-100 hover:text-orange-400"
				title={tab.name}
			>
				<p>{tab.name}</p>
			</a>
		{/each}
		<a
			href="https://github.com/ashishagarwal2023/CutYourURL"
			class="duration-200 hover:text-orange-400"
			target="_blank"
			title="CutYourURL GitHub"
		>
			<p><i class="fa-brands fa-github"></i></p>
		</a>
	</div>
	<a
		href="/try"
		class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950"
	>
		<div
					class="absolute top-0 right-full w-full h-full bg-orange-400 opacity-50 group-hover:translate-x-full z-0 duration-200"
				/>
				<h4 class="relative z-9 arrow-button hover:text-orange-900">Try it out! <i class="fa-solid fa-arrow-right px-1"></i></h4>
	</a>
</header>