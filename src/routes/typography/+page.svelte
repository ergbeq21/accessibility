<script>
	
	const chapters = [
        {
    number: 1,
    title: "The Importance of Accessible Typography",
    text: "Typography is not just a design choice—it’s a vital part of making digital content inclusive. Many users, particularly those with cognitive, visual, or reading disabilities, struggle to process text when typefaces, sizes, and spacing are not designed with accessibility in mind. Good typography helps all users read and understand content more easily, reducing cognitive load and frustration."
  },
  {
    number: 2,
    title: "Choosing the Right Typeface",
    text: "Select typefaces that are familiar, simple, and widely used, such as Arial or Verdana. These fonts have been shown to improve reading speed and comprehension for users with learning disorders like dyslexia or ADHD. Avoid ornate, script-style, or single-case fonts, which can cause confusion or slow down reading. Your goal should be clarity and ease, not decorative appeal."
  },
  {
    number: 3,
    title: "Clear Letterforms and Kerning",
    text: "Confusing characters such as the capital ‘I’, lowercase ‘l’, and the number ‘1’ should be clearly distinguishable. Likewise, ensure proper kerning—tight spacing can blur the line between letters, especially in problematic pairs like ‘r’ and ‘n’. This is crucial for readers with visual processing disorders, where minor design flaws can drastically affect comprehension."
  },
  {
    number: 4,
    title: "Font Size and Styling Techniques",
    text: "Font size should always use relative units like rem or em to support scalability for users who rely on browser zoom. Avoid overusing stylings such as italics, bold, or ALL CAPS, as they can reduce legibility and interfere with screen readers. Instead, use semantic HTML tags for emphasis and allow visual cues to support—but not replace—text meaning."
  },
  {
    number: 5,
    title: "Content Structure and Readability",
    text: "Typography doesn’t exist in isolation. Clear page structure with headings, paragraphs, lists, and appropriate spacing helps users navigate and understand content quickly. Avoid justified text alignment, which creates uneven spacing that distracts readers. Keep line widths narrow (under 80 characters) and separate visual sections with adequate spacing to improve flow and retention."
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

<section class="flex flex-col justify-center gap-10 p-10">
	  <h1 class="font-sans text-5xl font-extrabold text-center">
        Designing Inclusive <span class="text-indigo-500">Typography</span> for Accessibility
      </h1>
      <div class="flex flex-row gap-10 justify-center items-center">
        <button class="p-2 bg-indigo-500 hover:border rounded  hover:bg-white hover:text-black text-white transition-all duration-200 w-50 cursor-pointer font-mono"><a href="https://web.dev/learn/accessibility/typography?continue=https%3A%2F%2Fweb.dev%2Flearn%2Faccessibility%23article-https%3A%2F%2Fweb.dev%2Flearn%2Faccessibility%2Ftypography">Read full article</a></button>
        <button class="p-2 bg-white border rounded  hover:bg-indigo-500 hover:text-white transition-all duration-200 w-50 cursor-pointer font-mono"><a href="/article2">Go back</a></button>
      </div>

      

	<div class="flex h-100 flex-row gap-15">
		<ul class="flex w-100 flex-col gap-5">
			{#each chapters as chapter}
				<li class=" rounde border-gray-300 text-center text-black">
					<button
						class=" cursor-pointer border-b-1 p-5 font-mono text-xl font-bold"
						aria-controls={`chapter-${chapter.number}`}
						class:bg-indigo-500={selectedChapterNumber === chapter.number}
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

		<div class="w-[60%] mt-5">
			<p class="text-3xl font-light text-black">
				{selectedChapter.text}
			</p>
		</div>
	</div>

    
</section>

