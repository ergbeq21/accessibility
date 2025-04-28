

<script>
    import { ChevronDown, Rotate3D } from 'lucide-svelte';
    let {section, isExpanded ,  ...props} = $props();

    console.log(isExpanded);
</script>


<button class="flex flex-row items-center justify-between p-5 border-b-1 gap-4 w-300 cursor-pointer" {...props}>
    <div class="flex flex-col items-start gap-5 w-[80%]">
        <p class="font-bold">{section.title}</p>
        {#if isExpanded}
        <p class="text-start ">{section.text}</p>
        {/if}

    </div>
    <div class="transition-transform transform" class:rotate-180={isExpanded}>
        <ChevronDown size="20" />
    </div>
</button>
