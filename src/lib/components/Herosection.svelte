<script>
	import digitalAccess from '/src/assets/digitalAccss.png';
</script>

<section class="flex h-screen flex-row items-center justify-between">
	<div class="h-[100%] w-[50%] bg-gray-100">
		<h1 class="relative top-25 mb-6 text-center text-6xl font-extrabold text-indigo-700">
			Digital Accessibility<br /><span class="text-indigo-500">for Everyone</span>
		</h1>
		<img class="relative top-30 right-6" src={digitalAccess} alt="digital" />
	</div>

	<div class="flex h-[100%] w-[50%] flex-col items-center justify-between bg-black p-4 text-white">
		<div class="mt-20 flex flex-col items-center justify-center gap-10">
			<h1 class=" text-center font-sans text-7xl font-extrabold">
				Understanding Digital Accessibility
			</h1>
			<p class="relative text-center font-sans text-2xl font-extralight text-gray-300">
				Digital accessibility (a11y) ensures websites and apps are usable for people with
				disabilities. This course is designed for both beginner and advanced developers to learn
				accessibility practices, testing, and best practices. Explore topics with examples,
				references to standards like WCAG, and short assessments to solidify your understanding.
				Remember: true accessibility starts with listening to the needs of people with disabilities.
			</p>
			<button
				class="mt-4 w-100 cursor-pointer rounded border px-4 py-2 font-mono text-white transition-all duration-150 hover:bg-white hover:text-black"
			>
				<a href="/article2">Design and user experience </a>
			</button>
		</div>
	</div>
</section>
