<script lang="ts">
  import { onMount } from "svelte";

  import portfolioPhoto from "./assets/portfolio-design.jpeg";
  // import Scroller from "./lib/Scroller.svelte";

  let scrollers: NodeListOf<Element>;

  onMount(() => {
    scrollers = document.querySelectorAll<HTMLElement>(".scroller");

    if (!window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
      addAnimation();
    }
  });

  function addAnimation() {
    scrollers.forEach((scroller: HTMLElement) => {
      scroller.setAttribute("data-animated", "true");

      const scrollerInner =
        scroller.querySelector<HTMLElement>(".scroller__inner");
      const scrollerContent = Array.from(scrollerInner.children);

      scrollerContent.forEach((item) => {
        const duplicatedItem = item.cloneNode(true) as HTMLElement;
        duplicatedItem.setAttribute("aria-hidden", "true");
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
