<script lang="ts">
  import { onMount } from "svelte";

  import portfolioPhoto from "./assets/portfolio-design.jpeg";
  // import Scroller from "./lib/Scroller.svelte";

  let scrollers;

  onMount(() => {
    scrollers = document.querySelectorAll(".scroller");
    console.log(scrollers);

    if (!window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
      addAnimation();
    }
  });

  function addAnimation() {
    console.log("Im here inside addAnimation");
    scrollers.forEach((scroller) => {
      // add data-animated="true" to every `.scroller` on the page
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

<main class="card">
  <img class="photo" src={portfolioPhoto} alt="vcard profile" />

  <section>
    <header>
      <h1>Dante Solis</h1>
      <h3>
        Software Engineer
        {""}
        <br />
        UX/UI Designer
      </h3>
    </header>

    <div class="content">
      <p>
        I specialize in <span class="highlight">design systems</span> and crisp
        <span class="highlight">UI interfaces</span>, I turn ideas 💡 into
        websites and apps that keep users engaged.
      </p>
      <p>
        I combine extensive <span class="highlight">frontend experience</span>
        with a creative eye to deliver
        <span class="highlith">visually engaging </span>systems and products,
        helping startups and businesses define their identity and voice.
      </p>
    </div>

    <!-- [ERROR]: Causes problems with overflow -->
    <article class="scroller">
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
  </section>
</main>
