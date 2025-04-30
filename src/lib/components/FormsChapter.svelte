

<script>
    import MeasuredItem from "./measuredItem.svelte";

    const sections = [
        {
    title: "Overview",
    text: "Forms are essential UI components that let users enter data. They range from simple inputs to complex multi-step workflows. Making forms accessible is especially challenging because it involves not only correct markup but also considerations for assistive technologies, keyboard users, and users with cognitive impairments. This module introduces form-specific accessibility guidelines, complementing previously covered topics like focus management, content structure, and color contrast."
  },
  {
    title: "Fields",
    text: "Form fields are the interactive elements like text inputs, checkboxes, and radio buttons that users interact with. The best practice is to use native HTML form elements because they come with built-in accessibility features. Custom fields using ARIA should only be used when absolutely necessary and must follow specific rules to support screen readers and keyboard navigation effectively. Properly implemented fields improve the experience for all users, especially those relying on assistive technologies."
  },
  {
    title: "Autocomplete",
    text: "Using the `autocomplete` attribute on input fields helps browsers and assistive technologies predict user input. This improves form usability, reduces the chance of errors, and speeds up form completion. Autocomplete is especially helpful for users with memory or attention difficulties, and can be visually enhanced to provide meaningful feedback, like showing a birthday icon in a birthdate field. Correct use of autocomplete values contributes significantly to form accessibility and personalization."
  },
  {
    title: "Contextual Changes",
    text: "Forms should behave predictably. Avoid making contextual changes—such as submitting a form, navigating to a new page, or dynamically hiding elements—when a user simply focuses or inputs text into a field. If such changes are required, the user must be clearly informed ahead of time. Unexpected changes can confuse or disorient users, particularly those with cognitive disabilities or those using screen readers."
  },
  {
    title: "Labels",
    text: "Labels are vital for helping users understand what each form field is for. Every input must have a corresponding label that is visible and programmatically associated with the field. This helps screen readers communicate the field's purpose. Labels should also indicate if a field is required and provide any necessary instructions. Group related fields, such as address components, using semantic containers like `<fieldset>` and `<legend>` to improve both visual and screen reader accessibility."
  },
  {
    title: "Descriptions",
    text: "In some cases, labels alone aren’t enough. Field descriptions offer extra guidance, such as password requirements or input formats (e.g., MM-DD-YYYY). Use the `aria-describedby` attribute to link additional explanatory text to a form field. This ensures screen readers announce both the label and the description, reducing confusion and preventing input errors. Be careful not to use `aria-labelledby` to override essential label content unless it's intentional and tested."
  },
  {
    title: "Errors",
    text: "Users will make mistakes when filling out forms, and it's your responsibility to communicate these errors clearly and accessibly. Use inline messages, modals, or summary boxes to show what went wrong and how to fix it. Visually highlight the problematic fields and describe the issue in plain text. Use ARIA live regions to announce errors dynamically, and always allow users to resubmit once they've corrected the issues. Support both HTML5 validation (`required`, `pattern`) and ARIA (`aria-required`, `aria-invalid`) for broader accessibility."
  },
  {
    title: "Success Feedback",
    text: "After users correct errors and successfully submit a form, give them immediate, clear feedback—such as a success message or confirmation screen. This closure is important for all users but especially those using screen readers, as it verifies their task is complete. Success messages should be placed near the form or in an ARIA live region so assistive technologies can announce them."
  },
  {
    title: "WCAG 2.2 Criteria",
    text: "The latest Web Content Accessibility Guidelines (WCAG 2.2) introduce additional criteria for making forms more inclusive. These include ensuring that clickable targets meet minimum size requirements (Target Size), providing consistent access to help features (Consistent Help), avoiding reliance on memory or problem-solving for login (Accessible Authentication), and not requiring users to re-enter information they've already provided (Redundant Entry). Meeting these standards ensures broader accessibility and usability for everyone."
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
    <h1 class="font-extrabold text-7xl font-sans mt-10 text-center text-indigo-700">Accessible Form <span class="text-indigo-500">Design</span></h1>
    <div class="flex flex-col gap-4">
        {#each sections as section, index}
        <MeasuredItem {section} isExpanded={index === sectionExpanded} onclick={()=>{
            expland(index);
        }}/>
        {/each}
    </div>
    <div class="flex justify-center flex-row gap-10 mb-10 ">
        <button class="p-5  bg-indigo-700 text-white font-bold font-mono border hover:bg-white hover:text-black transition-all duration-300 cursor-pointer"><a href="https://web.dev/learn/accessibility/forms?continue=https%3A%2F%2Fweb.dev%2Flearn%2Faccessibility%23article-https%3A%2F%2Fweb.dev%2Flearn%2Faccessibility%2Fforms">
        Read full article
        </a></button>
        <button class="p-5 bg-white text-black font-bold font-mono border hover:bg-black hover:text-white transition-all duration-300 cursor-pointer"><a href="/article2">
            Go back
        </a></button>
    </div>
</section>