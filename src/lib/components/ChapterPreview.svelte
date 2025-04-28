<script>
	const chapters = [
		{
			number: 1,
			title: 'What is Digital Accessibility?',
			text: 'Learn the basics of a11y (accessibility), why it matters, and how it ensures websites and apps are inclusive for users with disabilities.'
		},
		{
			number: 2,
			title: 'Learning Paths for Developers',
			text: "This course supports both beginners and advanced developers.You'll find references to HTML and CSS fundamentals, helpful glossaries, and a flexible approach to learning accessibility topics at your own pace."
		},
		{
			number: 3,
			title: 'Building for Real Needs',
			text: "Understand how best practices may vary depending on different disabilities, and why it's crucial to listen to feedback from people with disabilities to create truly accessible experiences."
		}
	];

	let selectedChapterNumber = $state(1);

	let selectedChapter = $derived(
		chapters.find((chapter) => chapter.number === selectedChapterNumber)
	);

	function selectChapter(chapter) {
		selectedChapterNumber = chapter.number;
	}
</script>

<section class="flex flex-col justify-center gap-20 p-20">
	<h1 class="font-sans text-5xl font-extrabold" >
		Mastering the Essentials of <br />  Digital <span class="text-indigo-500"> Accessibility</span>
	</h1>

	<div class="flex h-100 flex-row gap-20">
		<ul class="flex w-[40%] flex-col gap-5">
			{#each chapters as chapter}
				<li class=" rounde border-gray-300 text-center text-black">
					<button
						class=" cursor-pointer border-b-1 p-5 font-mono text-2xl font-bold"
						aria-controls={`chapter-${chapter.number}`}
						class:bg-black={selectedChapterNumber === chapter.number}
						class:text-white={selectedChapterNumber === chapter.number}
						class:rounded={selectedChapterNumber === chapter.number}
						onclick={() => {
							selectChapter(chapter);
						}}
						aria-expanded={selectedChapterNumber === chapter.number}
					>
						<h3>Chapter {chapter.number}: {chapter.title}</h3>
					</button>
				</li>
			{/each}
		</ul>

		<div class="w-[40%]">
			<p class="text-3xl font-light text-black">
				{selectedChapter.text}
			</p>
		</div>
	</div>
</section>
