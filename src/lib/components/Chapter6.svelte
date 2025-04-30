<script>
    import img1 from "/src/assets/doc1.png";
    import img2 from "/src/assets/doc2.png";
    import img3 from "/src/assets/doc3.jpg";
  </script>
  
  <section id="chapter6" class="min-h-screen flex flex-col px-8 py-12 bg-gradient-to-br from-white via-blue-50 to-blue-100 text-gray-800 font-sans">
  
    <div class="flex flex-row items-center gap-8 mb-16">
      <img src={img1} alt="" class="w-1/2 rounded-xl shadow-md object-cover" />
      <div class="flex flex-col gap-6 w-1/2">
        <h1 class="text-4xl font-bold text-blue-700">Document Accessibility</h1>
        <p class="text-lg">
          This module explains specific HTML elements essential for digital accessibility, building on basic HTML knowledge.
        </p>
        <p class="text-blue-500 font-medium text-lg">Focus areas: Page Titles, Language Attributes, and iFrames</p>
  
        <div class="flex gap-4 mt-4">
          <img src={img2} alt="" class="w-80 h-45 rounded shadow" />
          <img src={img3} alt="" class="w-80 h-45 rounded shadow" />
        </div>
      </div>
    </div>
  
    <div class="text-center">
      <h2 class="text-3xl font-semibold text-gray-700 mb-10">Key Accessibility Elements</h2>
      <div class="grid grid-cols-3 gap-8">
        <div class="bg-white rounded-lg p-6 shadow hover:shadow-lg transition">
          <h3 class="text-xl font-semibold text-blue-600 mb-2">Page Title</h3>
          <p class="text-gray-600">
            The <code>&lt;title&gt;</code> tag defines the page's content, important for both screen readers and SEO. Keep it accurate, concise, and front-loaded with relevant info.
          </p>
        </div>
        <div class="bg-white rounded-lg p-6 shadow hover:shadow-lg transition">
          <h3 class="text-xl font-semibold text-blue-600 mb-2">Language Attributes</h3>
          <p class="text-gray-600">
            Use <code>lang</code> in the <code>&lt;html&gt;</code> tag to set the page's primary language. For multilingual content, apply <code>lang</code> to individual elements as needed.
          </p>
        </div>
        <div class="bg-white rounded-lg p-6 shadow hover:shadow-lg transition">
          <h3 class="text-xl font-semibold text-blue-600 mb-2">iFrames</h3>
          <p class="text-gray-600">
            Include a descriptive <code>title</code> in <code>&lt;iframe&gt;</code> tags for screen readers, and enable scrolling to improve accessibility for all users.
          </p>
        </div>
      </div>
    </div>
  </section>
  