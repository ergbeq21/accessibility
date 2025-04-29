<script>
    import digitalAccess from '/src/assets/digitalAccss.png';
    import audio from '/src/assets/audio.webp';
    import forms from '/src/assets/forms.webp';
    import typography from '/src/assets/typography.png';
    import design from '/src/assets/design.webp';
    import UserDes from '/src/assets/accessDesign.avif'
    import form from '/src/assets/form.png';

    const accessibilityChapters = [
  {
    title: "Typography",
    image: typography,
    link: "/typography",
    text: "Explore how accessible typography improves readability for all users, including those with dyslexia or low vision. Learn best practices for font choices, size, spacing, and contrast to create inclusive digital content."
  },
  {
    title: "Forms",
    image: form,
    link: "/forms",
    text: "Accessible forms are essential for user interaction. Discover how to label inputs properly, provide helpful error messages, and ensure keyboard navigation works seamlessly for screen reader users and those with motor impairments."
  },
  {
    title: "Design and User Experience",
    image: UserDes,
    link: "/designUser",
    text: "Learn how inclusive design enhances user experience for everyone. This section covers color contrast, intuitive navigation, responsive layouts, and how to design for assistive technology compatibility."
  },
  {
    title: "Video and Audio",
    image: audio,
    link: "/videoAudio",
    text: "Accessible multimedia ensures that video and audio content can be understood by all. Understand the importance of captions, transcripts, audio descriptions, and accessible players for users who are deaf, hard of hearing, or blind."
  }
];
</script>




<section class="min-h-screen flex flex-col gap-7 m-15 mt-10 items-center justify-center">

    <div class="w-full flex flex-col gap-5 ml-30">
      <h1 class="text-6xl font-extrabold text-indigo-500">
        Learn About the <span class='text-indigo-700'>Core Sections</span> of <br> Accessibility  
      </h1>
      <p class="text-2xl font-extralight">
        Gain a thorough understanding of digital accessibility through our in-depth exploration  
      </p>
      <a href="/" class="w-50 text-center p-2 bg-indigo-600 rounded text-white font-light hover:bg-indigo-700 transition">
        Go back
      </a>
    </div>
  
    <div class="grid grid-cols-2 gap-5 w-full">
        {#each accessibilityChapters as chapter}
      <div class="p-5 rounded ml-10 w-150">
        <h1 class=" mb-3 font-bold text-3xl text-indigo-600">{chapter.title}</h1>
        <a href={chapter.link}>
          <img
          src={chapter.image}
          alt=""
          class="mb-6 h-72 w-130 rounded-2xl object-cover shadow border border-gray-200 hover:scale-102 transition-transform duration-300 ease-in-out"
        />  
        </a>
        <p class="w-130"><a href="/typography" class=" font-extralight text-s">{chapter.text}</a></p>
      </div>
      {/each}

    </div>
  
  </section>
  