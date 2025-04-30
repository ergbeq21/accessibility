<script>
    import htmlAria from "/src/assets/AriaHtml.jpg";
  </script>
  
  <section id="chapter4" class="min-h-screen bg-gray-50 py-16 px-12 flex flex-col justify-center items-center text-gray-800">  
    <div class="flex flex-row gap-10">
      <div class="w-full text-center space-y-7 flex flex-col justify-center items-start">
        <div class="flex flex-col gap-2 justify-center items-start">
          <h1 class="text-5xl font-extrabold decoration-blue-500">Chapter 4: HTML & ARIA</h1>
          <div class="bg-indigo-500 w-150 h-1"></div>
        </div>
  
        <p class="text-xl text-gray-600 text-start">
          ARIA (Accessible Rich Internet Applications) is a set of attributes that enhance accessibility for users who rely on assistive technologies like screen readers. It communicates roles, properties, and states to the accessibility tree, helping users navigate dynamic content and custom UI elements.
        </p>
        <p class="text-blue-600 font-semibold text-lg">Understanding ARIA in HTML</p>
      </div>
  
      <div class="my-12 w-full max-w-4xl">
        <img src={htmlAria} alt="html and aria" class="rounded-xl shadow-lg w-full object-cover hover:scale-95 transition-all duration-300" />
      </div>
    </div>
  
     <div class="space-y-6 text-center bg-indigo-600 w-full flex justify-center items-start flex-col p-7 text-white rounded-2xl">
      <h2 class="text-3xl font-semibold">Why This Matters</h2>
      <p class="text-lg text-white text-start">
        While HTML5 provides built-in accessibility with semantic elements, ARIA becomes essential when standard HTML falls short—such as in complex components or when browser support is limited. But misuse can cause more harm than good.
      </p>
      <p class="text-white font-medium text-start">
        Follow the WAI’s five rules of ARIA: prioritize semantic HTML, avoid unnecessary ARIA, ensure keyboard accessibility, don’t hide focusable elements, and always use accessible names. Used correctly, ARIA empowers inclusive, equitable digital experiences.
      </p>
    </div>
  </section>
  