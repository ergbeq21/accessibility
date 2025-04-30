<script>
	import Herosection from '$lib/components/Herosection.svelte';
	import ChapterPreview from '$lib/components/ChapterPreview.svelte';
	import MeasuredChapter from '$lib/components/measuredChapter.svelte';
	import Chapter2 from '$lib/components/Chapter2.svelte';
	import Chapter3 from '$lib/components/Chapter3.svelte';
	import Chapter4 from '$lib/components/Chapter4.svelte';
	import Chapter5 from '$lib/components/Chapter5.svelte';
	import Chapter6 from '$lib/components/Chapter6.svelte';
</script>



<nav class="w-full bg-transparent">
	<div class="flex justify-center items-center">
		<ul class="fixed top-1 left-1/2 -translate-x-1/2 flex flex-wrap justify-center items-center gap-5 px-6 py-3 
		bg-white/60 backdrop-blur-md shadow-md rounded-full text-black text-base font-semibold z-50">
	 <li><a href="/" class="hover:text-blue-600 transition">Home</a></li>
	 <li><a href="#chapter2" class="hover:text-blue-600 transition">Usability</a></li>
	 <li><a href="#chapter3" class="hover:text-blue-600 transition">Metrics</a></li>
	 <li><a href="#chapter4" class="hover:text-blue-600 transition">AriaHtml</a></li>
	 <li><a href="#chapter5" class="hover:text-blue-600 transition">Layout</a></li>
	 <li><a href="#chapter6" class="hover:text-blue-600 transition">Document</a></li>
   </ul>

</div>

  
  </nav>

<Herosection />
<ChapterPreview />
<Chapter2/>
<Chapter3/>
<Chapter4/>
<Chapter5/>
<Chapter6/>






