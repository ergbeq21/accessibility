

<script>
    import MeasuredItem from "./measuredItem.svelte";

    const sections = [

    {
    title: "What is Inclusive Design?",
    text: "Inclusive design is a human-centered approach that integrates accessibility, usability, and inclusivity. It acknowledges the diverse ways people interact with digital interfaces and strives to create experiences that accommodate all users. This includes users with disabilities, those in varying environments, and those using different devices. The goal is to make digital products functional, accessible, and meaningful for everyone."
  },
  {
    title: "Inclusive vs. Universal Design",
    text: "Inclusive design differs from universal design in its methodology. While universal design attempts to create one solution for as many people as possible, inclusive design starts with specific use cases or individuals—particularly those with unique needs—and adapts the solution outward to serve a wider group. This targeted approach ensures that overlooked or marginalized users are considered from the start, resulting in more flexible and robust designs."
  },
  {
    title: "Key Inclusive Design Principles",
    text: "There are seven main principles of inclusive design that help guide decision-making: 1) Provide comparable experiences to all users; 2) Consider different contexts and situations users may be in; 3) Use consistent and predictable patterns; 4) Give users control over how they interact with the content; 5) Offer multiple ways to complete tasks; 6) Prioritize essential content and features to avoid distractions; 7) Add value to user experiences by making thoughtful design choices that enhance usability and accessibility."
  },
  {
    title: "Using Personas",
    text: "User personas are fictional profiles based on research that represent different types of users. They help teams visualize and empathize with their audience. Inclusive design recommends integrating disabilities—both permanent and temporary—into these personas. This helps teams better anticipate accessibility needs and make more inclusive design decisions. However, it is important to avoid stereotypes and to base personas on real data. Personas are a complement to, not a replacement for, user testing."
  },
  {
    title: "Caution with Disability Simulators",
    text: "Disability simulators are tools that attempt to mimic the experience of having a disability. While they can help some understand challenges, they can also be misleading or reduce complex experiences to simplified interactions. Many accessibility advocates prefer using firsthand content—such as videos, interviews, and articles—created by people with disabilities to gain real insight into their needs and experiences. It's important to approach simulation with care and not let it replace authentic learning."
  },
  {
    title: "Accessibility Heuristics",
    text: "Accessibility heuristics are a set of principles designed to guide inclusive interaction design. Originating from usability heuristics, these updated guidelines focus on digital accessibility. They include areas such as allowing multiple input methods, supporting clear navigation, ensuring content structure is meaningful, preventing errors, providing legible and readable text, maintaining consistency, supporting time-based tasks, avoiding harmful animations, and offering alternatives for visual and audio content. Implementing these can eliminate a majority of accessibility issues before development begins."
  },
  {
    title: "Accessibility Annotations",
    text: "Accessibility annotations are notes added to design files to guide developers in implementing accessible features. These annotations explain how different components should behave, how to structure content semantically, and how to meet accessibility standards. They can include information on contrast ratios, button states, alt text, keyboard navigation, headings, form labels, and more. Including annotations during the design handoff ensures that the final product retains its intended accessibility and usability features across all user scenarios."
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
    <h1 class="font-extrabold text-7xl font-sans mt-10 text-center text-indigo-700">Design and <span class="text-indigo-500">user</span> experience</h1>
    <div class="flex flex-col gap-4">
        {#each sections as section, index}
        <MeasuredItem {section} isExpanded={index === sectionExpanded} onclick={()=>{
            expland(index);
        }}/>
        {/each}
    </div>
    <div class="flex justify-center flex-row gap-10 mb-10 ">
        <button class="p-5  bg-indigo-700 text-white font-bold font-mono border hover:bg-white hover:text-black transition-all duration-300 cursor-pointer"><a href="https://web.dev/learn/accessibility/design-ux?continue=https%3A%2F%2Fweb.dev%2Flearn%2Faccessibility%23article-https%3A%2F%2Fweb.dev%2Flearn%2Faccessibility%2Fdesign-ux">
        Read full article
        </a></button>
        <button class="p-5 bg-white text-black font-bold font-mono border hover:bg-black hover:text-white transition-all duration-300 cursor-pointer"><a href="/">
            Go to home page
        </a></button>
    </div>
</section>