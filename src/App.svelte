<script lang="ts">
  import portfolioPhoto from "./assets/portfolio-design.jpeg";
  import Scroller from "./lib/Scroller.svelte";
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
        <span class="highlight">visually engaging </span>systems and products,
        helping startups and businesses define their identity and voice.
      </p>
    </div>

    <Scroller />
  </section>
</main>
