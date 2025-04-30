<script>
	
	const chapters = [
        {
    number: 1,
    title: "Introduction to Accessible Media",
    text: "Ensuring accessibility in audio and video content is essential for creating inclusive digital experiences. People with disabilities—such as hearing loss, visual impairment, or cognitive challenges—often rely on alternative media formats like captions, transcripts, and audio descriptions. While not everyone is directly involved in media production, it's important for developers and designers to understand these requirements to create proper layouts and user experiences that support accessibility standards."
  },
  {
    number: 2,
    title: "Captions",
    text: "Captions are synchronized text displays that provide spoken dialogue and important sounds in videos for users who are deaf or hard of hearing. There are two types: closed captions, which can be toggled on or off, and open captions, which are always visible and embedded into the video. Captions also benefit users in noisy environments, those learning new languages, or anyone watching content without sound. They differ from subtitles, which typically translate dialogue but don’t include sound effects or speaker identification."
  },
  {
    number: 3,
    title: "Transcripts",
    text: "Transcripts are detailed text documents containing all spoken content and relevant visual cues from audio or video files. They serve users who are deaf, deafblind, or who prefer reading over listening. Transcripts are also beneficial for search engine optimization, as search engines can index their content. Providing transcripts ensures that users can access information at their own pace, and they can be included inline on the page, as downloadable files, or linked through the video description."
  },
  {
    number: 4,
    title: "Audio Descriptions",
    text: "Audio descriptions provide a narration of important visual elements in video content, such as facial expressions, scene changes, or silent actions. This helps users who are blind or have low vision to fully understand the visual aspects of the media. In cases where normal video timing doesn’t allow enough room for descriptions, extended audio descriptions can be used, where the video pauses temporarily for the narration to catch up before resuming playback."
  },
  {
    number: 5,
    title: "Sign Language Interpretation",
    text: "Sign language interpretation involves a live or recorded interpreter translating audio content into sign language. It provides access for users whose primary language is sign language, offering a more natural and expressive format than text alone. While sign language is extremely helpful, the high cost and variety of sign languages around the world can pose challenges. It's important to consider your audience and resources when deciding whether to include sign language interpretation in your media."
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
        Ensuring Accessibility<span class="text-indigo-500">in Video and </span> Audio Content
      </h1>
      <div class="flex flex-row gap-10 justify-center items-center">
        <button class="p-2 bg-indigo-500 hover:border rounded  hover:bg-white hover:text-black text-white transition-all duration-200 w-50 cursor-pointer font-mono"><a href="https://web.dev/learn/accessibility/video-audio?continue=https%3A%2F%2Fweb.dev%2Flearn%2Faccessibility%23article-https%3A%2F%2Fweb.dev%2Flearn%2Faccessibility%2Fvideo-audio">Read full article</a></button>
        <button class="p-2 bg-white border rounded  hover:bg-indigo-500 hover:text-white transition-all duration-200 w-50 cursor-pointer font-mono"><a href="/article2">Go back</a></button>
      </div>

      

	<div class="flex h-100 flex-row gap-15">
		<ul class="flex flex-col gap-5">
			{#each chapters as chapter}
				<li class=" rounde border-gray-300 text-center text-black">
					<button
						class=" cursor-pointer border-b-1 p-5 font-mono text-xl font-bold w-110"
						class:bg-indigo-500={selectedChapterNumber === chapter.number}
						class:text-white={selectedChapterNumber === chapter.number}
						class:rounded={selectedChapterNumber === chapter.number}
						onclick={() => {
							selectChapter(chapter);
						}}
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

