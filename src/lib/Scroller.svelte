<script lang="ts">
  
  import { onMount } from 'svelte';

  let scrollers;

  onMount(() => {
    scrollers = document.querySelectorAll(".scroller");
    console.log(scrollers);

    if (!window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
      addAnimation();
    }
  });


function addAnimation() {
  console.log('Im here inside addAnimation')
  scrollers.forEach((scroller) => {

    scroller.setAttribute("data-animated", true);

    // console.log(scroller, 'scroller');

    // Make an array from the elements within `.scroller-inner`
    const scrollerInner = scroller.querySelector(".scroller__inner");
    const scrollerContent = Array.from(scrollerInner.children);

    // For each item in the array, clone it
    // add aria-hidden to it
    // add it into the `.scroller-inner`
    scrollerContent.forEach((item) => {
      const duplicatedItem = item.cloneNode(true);
      duplicatedItem.setAttribute("aria-hidden", true);
      scrollerInner.appendChild(duplicatedItem);
    });
  });
}
</script>