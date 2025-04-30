<script>
    import structure from '/src/assets/structute.png';
</script>

<h1 class="font-extrabold text-6xl text-center text-indigo-600"  id="chapter5">Content structure</h1>

<section class="min-h-screen flex flex-row gap-10 m-8">

    <div class="flex flex-col gap-6 w-2/3">
        <img src={structure} alt="Website Content Structure Diagram" class="rounded-xl shadow-lg object-cover w-full max-h-[500px]" />

        <div class="bg-white p-6 rounded-xl shadow-md border border-gray-200">
            <h1 class="text-2xl font-semibold text-gray-800 mb-2">
                Structuring Web Content for Accessibility and Clarity
            </h1>
            <p class="text-sm text-gray-500 mb-4">CONTENT STRUCTURE • 20 MIN READ</p>
            <p class="text-base text-gray-700 mb-3">
                A well-organized content structure is essential for building accessible and user-friendly web pages. This layout demonstrates a clear division between main content and supplemental navigation, improving both usability and readability.
            </p>
            <p class="text-base text-gray-700 mb-3">
                On the left side, a central image illustrates the idea of structural layout in web design. Below it, the featured article includes a descriptive heading and category label, reinforcing the importance of using semantic HTML elements such as headings and paragraphs to guide the user through the content.
            </p>
            <p class="text-base text-gray-700 mb-3">
                On the right side, a "Most Popular" section displays four highlighted articles, each with a bold title and a short description. This sidebar supports quick navigation and improves content discovery.
            </p>
            <p class="text-base text-gray-700">
                The combination of proper headings, spacing, and layout in this section helps deliver a visually balanced and accessible experience for all users, including those using assistive technologies.
            </p>
        </div>
    </div>

    <div class="flex flex-col gap-6 w-1/3">
        <h2 class="text-xl font-bold border-b text-indigo-500">Most Popular</h2>
    
        <div class="bg-gray-50 p-4 rounded-lg shadow-sm hover:shadow-md transition">
            <h3 class="text-lg font-semibold text-gray-800">How to Create a Responsive Layout</h3>
            <p class="text-sm text-gray-600 mt-1">Learn the basics of building responsive designs with modern CSS techniques.</p>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg shadow-sm hover:shadow-md transition">
            <h3 class="text-lg font-semibold text-gray-800">Improving Web Accessibility</h3>
            <p class="text-sm text-gray-600 mt-1">Explore practical steps to make your website more accessible for all users.</p>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg shadow-sm hover:shadow-md transition">
            <h3 class="text-lg font-semibold text-gray-800">Semantic HTML in Practice</h3>
            <p class="text-sm text-gray-600 mt-1">Discover how semantic tags improve SEO and screen reader compatibility.</p>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg shadow-sm hover:shadow-md transition">
            <h3 class="text-lg font-semibold text-gray-800">Designing with Users in Mind</h3>
            <p class="text-sm text-gray-600 mt-1">Understand the principles of user-centered design and content organization.</p>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg shadow-sm hover:shadow-md transition">
            <h3 class="text-lg font-semibold text-gray-800">Optimizing Images for Web</h3>
            <p class="text-sm text-gray-600 mt-1">Techniques for compressing and serving images without losing quality.</p>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg shadow-sm hover:shadow-md transition">
            <h3 class="text-lg font-semibold text-gray-800">Using Tailwind CSS Efficiently</h3>
            <p class="text-sm text-gray-600 mt-1">Tips for organizing utility classes and managing design consistency.</p>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg shadow-sm hover:shadow-md transition">
            <h3 class="text-lg font-semibold text-gray-800">Building Accessible Forms</h3>
            <p class="text-sm text-gray-600 mt-1">Best practices for labeling, validation, and keyboard navigation.</p>
        </div>
    </div>
    
    
</section>
