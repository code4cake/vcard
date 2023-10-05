<script lang="ts">
  import { onMount } from "svelte";

  import "./scroller.css";

  let scroller: HTMLElement | null = null;

  onMount(() => {
    scroller = document.querySelector<HTMLElement>(".scroller");

    if (!window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
      addAnimation(scroller);
    }
  });

  function addAnimation(element: HTMLElement) {
    element.setAttribute("data-animated", "true");

    const scrollerInner =
      element.querySelector<HTMLElement>(".scroller__inner");

    const scrollerContent = Array.from(scrollerInner.children);

    scrollerContent.forEach((item) => {
      const duplicatedItem = item.cloneNode(true) as HTMLElement;
      duplicatedItem.setAttribute("aria-hidden", "true");
      scrollerInner.appendChild(duplicatedItem);
    });
  }
</script>

<article bind:this={scroller} class="scroller">
  <ul class="tag-list scroller__inner">
    <li>Javascript</li>
    <li>Typescript</li>
    <li>React</li>
    <li>React Redux</li>
    <li>NextJs</li>
    <li>Svelte</li>
    <li>CSS</li>
    <li>CSS in JS</li>
    <li>UX /UI</li>
    <li>Figma</li>
    <li>Framer</li>
    <li>InDesign</li>
    <li>Illustrator</li>
  </ul>
</article>
