

<script>
    import MeasuredItem from "./measuredItem.svelte";

    const sections = [
  {
    title: "Introduction to Accessibility Testing",
    text: "Accessibility testing involves checking digital products against recognized standards to ensure they are usable by people with disabilities. The industry, local laws, or project goals often determine which standard to use, but the Web Content Accessibility Guidelines (WCAG) are commonly recommended. Accessibility audits, using automated, manual, design, and assistive technology testing, should be conducted regularly throughout a product’s lifecycle to maintain compliance."
  },
  {
    title: "Understanding the Web Content Accessibility Guidelines (WCAG)",
    text: "WCAG, developed by the W3C, provides a global standard for digital accessibility. Primarily targeting web and mobile app creators, WCAG outlines success criteria across three levels: A, AA, and AAA. To achieve a higher level like AA, a product must meet both A and AA criteria. WCAG 2.2 is the current standard, with WCAG 3.0 still in draft form. Following these guidelines ensures a broader, more accessible reach for digital content."
  },
  {
    title: "Accessibility Principles: The POUR Framework",
    text: "The POUR principles—Perceivable, Operable, Understandable, and Robust—offer a foundational way to think about accessibility beyond technical rules. They focus on real human experiences and guide the creation of inclusive digital products."
  },
  {
    title: "Perceivable: Making Content Available to the Senses",
    text: "The Perceivable principle ensures that users can see, hear, or otherwise sense all essential content. This includes providing text alternatives for images, captions for videos, and ensuring color is not the only way information is conveyed. The goal is to make sure no user is excluded based on sensory disability."
  },
  {
    title: "Operable: Ensuring Usable Interfaces",
    text: "Operability requires that all users can navigate and interact with a digital product. Interfaces must support keyboard navigation, touchscreens, and avoid 'keyboard traps' where users get stuck. Features like giving users enough time to complete tasks and ensuring all controls are accessible help meet this standard."
  },
  {
    title: "Understandable: Making Information Clear and Predictable",
    text: "An understandable digital product presents information and navigation that users can easily grasp. This involves writing in simple language, maintaining predictable layouts, and ensuring that error messages are straightforward and actionable. The goal is to reduce confusion and make interaction effortless for all users."
  },
  {
    title: "Robust: Supporting a Range of Technologies",
    text: "Robustness ensures that digital products work with various assistive technologies and remain accessible as technology evolves. Testing with different screen readers, ensuring keyboard-only functionality, and maintaining compatibility across devices and orientations are crucial parts of building a robust experience."
  },
  {
    title: "Conclusion: Focusing on Human Needs",
    text: "Ultimately, the POUR principles are about more than strict rules—they are a way to meet the diverse needs of users. By focusing on perceivability, operability, understandability, and robustness, developers and designers can create truly inclusive digital experiences."
  }
];


let sectionExpanded = $state(-1);

function expland(index){
    if(sectionExpanded == index){
        sectionExpanded = -1;
    }else{

        sectionExpanded = index;

    }
}

</script>


<section class="flex flex-col gap-20">
    <h1 class="font-extrabold text-7xl font-sans mt-10 text-center text-indigo-700">How is digital <span class="text-indigo-500">accessibility</span> measured?</h1>
    <div class="flex flex-col gap-4">
        {#each sections as section, index}
        <MeasuredItem {section} isExpanded={index === sectionExpanded} onclick={()=>{
            expland(index);
        }}/>
        {/each}
    </div>
    <div class="flex justify-center flex-row gap-10 mb-10 ">
        <button class="p-5  bg-indigo-700 text-white font-bold font-mono border hover:bg-white hover:text-black transition-all duration-300 cursor-pointer"><a href="https://web.dev/learn/accessibility/measure?continue=https%3A%2F%2Fweb.dev%2Flearn%2Faccessibility%23article-https%3A%2F%2Fweb.dev%2Flearn%2Faccessibility%2Fmeasure">
        Read full article
        </a></button>
        <button class="p-5 bg-white text-black font-bold font-mono border hover:bg-black hover:text-white transition-all duration-300 cursor-pointer"><a href="/">
            Go to home page
        </a></button>
    </div>
</section>