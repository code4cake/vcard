<script lang="ts">
  // import svelteLogo from './assets/svelte.svg'
  // import viteLogo from '/vite.svg'
  // import Counter from './lib/Counter.svelte'
  // import Icon from '@iconify/svelte'
  import portfolioPhoto from './assets/portfolio-design.jpeg'
  import DribbleIcon from './assets/dribble-icon.svg';
</script>

<header>
  <ul class='list'>
    <li class='list__item'>
      <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 1000 1000"><path d="M0 500c0-90.667 22.334-174.333 67-251 44.667-76.667 105.334-137.333 182-182C325.667 22.333 409.334 0 500 0c90.667 0 174.334 22.333 251 67 76.667 44.667 137.334 105.333 182 182 44.667 76.667 67 160.333 67 251s-22.333 174.333-67 251c-44.666 76.667-105.333 137.333-182 182-76.666 44.667-160.333 67-251 67-90.666 0-174.333-22.333-251-67-76.666-44.667-137.333-105.333-182-182C22.334 674.333 0 590.667 0 500zm83 0c0 104 35 195.667 105 275 32-62.667 82.667-122.333 152-179 69.334-56.667 137-92.333 203-107-10-23.333-19.666-44.333-29-63-114.666 36.667-238.666 55-372 55-26 0-45.333-.333-58-1 0 2.667-.166 6-.5 10-.333 4-.5 7.333-.5 10zm13-103c14.667 1.333 36.334 2 65 2 111.334 0 217-15 317-45-50.666-90-106.333-165-167-225-52.666 26.667-97.833 63.667-135.5 111-37.666 47.333-64.166 99.667-79.5 157zm149 432c75.334 58.667 160.334 88 255 88 49.334 0 98.334-9.333 147-28-13.333-114-39.333-224.333-78-331-61.333 13.333-123.166 47-185.5 101C321.167 713 275 769.667 245 829zM398 97c58.667 60.667 113 136.333 163 227 90.667-38 159-86.333 205-145-77.333-64-166-96-266-96-34 0-68 4.667-102 14zm199 298c10 21.333 21.334 48.333 34 81 49.334-4.667 103-7 161-7 41.334 0 82.334 1 123 3-5.333-90.667-38-171.333-98-242-43.333 64.667-116.666 119.667-220 165zm59 151c34 98.667 57 200 69 304 52.667-34 95.667-77.667 129-131 33.334-53.333 53.334-111 60-173-48.666-3.333-93-5-133-5-36.666 0-78.333 1.667-125 5z"/></svg>
    </li>
    <li class="list__item"><a href="/">Home</a></li>
  </ul>
</header>
<main>


  <!-- <div class="card"> -->
    <img class="photo" src={portfolioPhoto} alt="vcard profile">
  <!-- </div> -->

  <section>
    <header>
      <h1>Dante Solis</h1>
      <h3>
        Software Engineer 
        {""} 
        <br />
        UX/UI Designer
      </h3>
      <!-- <h3>UX/UI Designer </h3> -->
    </header>

    <div class="content">
      <p> I specialize in <span class="highlight">design systems</span> and crisp <span class="highlight">UI interfaces</span>,  I turn ideas 💡  into websites and apps that keep users engaged. </p>
      <p> I combine extensive <span class="highlight">frontend experience</span> with a creative eye to deliver <span class="highlith">visually engaging </span>systems and products, helping startups and businesses define their identity and voice</p>
    </div>


    <article class="scroller">
      <ul class="list-tech">
        <li class='list-tech__item'>Javascript</li>  
        <li class='list-tech__item'>Typescript</li>
        <li class='list-tech__item'>React</li>
        <li class='list-tech__item'>React Redux</li>
        <li class='list-tech__item'>NextJs</li>
        <li class='list-tech__item'>Svelte</li>
        <li class='list-tech__item'>Figma</li>
        <li class='list-tech__item'>Framer</li>
        <li class='list-tech__item'>Adobe InDesign</li>
        <li class='list-tech__item'>Adobe Illustrator</li>
      </ul>
    </article>
  
  </section>



  <!-- <div>
    <a href="https://vitejs.dev" target="_blank" rel="noreferrer">
      <img src={viteLogo} class="logo" alt="Vite Logo" />
    </a>
    <a href="https://svelte.dev" target="_blank" rel="noreferrer">
      <img src={svelteLogo} class="logo svelte" alt="Svelte Logo" />
    </a>
  </div>
  <h1>Vite + Svelte</h1>

  <div class="card">
    <Counter />
  </div>

  <p>
    Check out <a href="https://github.com/sveltejs/kit#readme" target="_blank" rel="noreferrer">SvelteKit</a>, the official Svelte app framework powered by Vite!
  </p>

  <p class="read-the-docs">
    Click on the Vite and Svelte logos to learn more
  </p> -->
</main>

<style>
  /* .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  } */
</style>
