<script>
  let activeWindow = 'desktop';
  
  function openWindow(windowName) {
    activeWindow = windowName;
  }
  function closeWindow() {
    activeWindow = 'desktop';
  }
</script>

<main>
  <div class="window-container">
    <div class="window-head">
      <p>alex cmsc 57 ePortfolio !!</p>
    </div>
    <div class="main-window">

      {#if activeWindow === 'desktop'}
      <!-- main desktop page -->
      <div class="icon-row">
        <div class="desktop-icon-container" on:click={() => openWindow('counting')} on:keydown={(e) => e.key === 'Enter' && openWindow('counting')} role="button" tabindex="0">
          <div class="desktop-icon counting"></div>
          <p class="icon-title">Counting</p>
        </div>

        <div class="desktop-icon-container" on:click={() => openWindow('algebraic-structures')} on:keydown={(e) => e.key === 'Enter' && openWindow('algebraic-structures')} role="button" tabindex="0">
          <div class="desktop-icon algebraic-structures"></div>
          <p class="icon-title">Algebraic Structures and Groups</p>
        </div>

        <div class="desktop-icon-container" on:click={() => openWindow('groups-rings-fields')} on:keydown={(e) => e.key === 'Enter' && openWindow('groups-rings-fields')} role="button" tabindex="0">
          <div class="desktop-icon groups-rings-fields"></div>
          <p class="icon-title">Groups, Rings, & Fields</p>
        </div>

        <div class="desktop-icon-container" on:click={() => openWindow('discrete-probability')} on:keydown={(e) => e.key === 'Enter' && openWindow('discrete-probability')} role="button" tabindex="0">
          <div class="desktop-icon discrete-probability"></div>
          <p class="icon-title">Discrete Probability</p>
        </div>

        <div class="desktop-icon-container" on:click={() => openWindow('graphs')} on:keydown={(e) => e.key === 'Enter' && openWindow('graphs')} role="button" tabindex="0">
          <div class="desktop-icon graphs"></div>
          <p class="icon-title">Graphs</p>
        </div>
      </div>
      
        {:else if activeWindow === 'counting'}
      <!-- counting window -->
       <div class="content-window">
        <div class="content-header">
          <h2>Counting</h2>
          <button on:click={closeWindow} class="close-button">X</button>
        </div>
        <div class="scrollable-content">

          <p>I remember the first time <b>counting</b> was mentioned. It was a funny moment, because "counting" sounds like something straight out of a kid's learning exercise. 
            Of course, it wasn't just counting digits from 1-100, but something a little more complex.</p>
          <p>It was about <b>counting possibilities</b>, how many ways something <i>can</i> happen, and how many ways it <i>can’t</i>.
             Suddenly, “counting” wasn’t just about how many fingers you could count up to in kindergarten. It was about factorials, permutations, combinations, and the pigeonhole principle, 
             tools for solving problems that look simple until you realize they’re layered with logic.  </p>
          <p>After a while, I realized that counting followed me everywhere, as a Computer Science student and as a developing developer.</p>
          <p>I realized that, what started as a funny name in class turned out to be one of the most useful skills a Computer Scientist should have.</p>
        </div>
       </div>

        {:else if activeWindow === 'algebraic-structures'}
      <!-- algebraic structures window -->
       <div class="content-window">
        <div class="content-header">
          <h2>Algebraic Structures and Groups</h2>
          <button on:click={closeWindow} class="close-button">X</button>
        </div>
        <div class="scrollable-content">

          <p>Algebraic structures, at first glance, seem really <b>abstract</b>, which makes sense since it's basically an introduction to abstract algebra. 
            Groups were an interesting concept to make my head wrap around. (still confuses me)</p>

          <p>I realized that, algebraic structures were something I've already seen before. For example, shape rotations in graphic design, that's an example of an application of group theory. Vector space translations, something that's widely used in artificial intelligence infrastructure, was an application of that "rotation."</p>
          
          <p>As I went through the material, I realized that I've "played these games" before, and even without going through the course,
             I was able to understand what they were for back then.</p>
          <p>CMSC 57 gave me the vocabulary and structure to help me describe them better than I did before.</p>
          <!--ADD MORE CONTENT-->

        </div>
       </div>

        {:else if activeWindow === 'groups-rings-fields'}
      <!-- groups, rings, and fields window -->
       <div class="content-window">
        <div class="content-header">
          <h2>Groups, Rings, & Fields</h2>
          <button on:click={closeWindow} class="close-button">X</button>
        </div>
        <div class="scrollable-content">

          <p>Similar to algebraic structures, it sounded like a bunch of abstract math jargon. Something I'd probably never encounter in life if I never took Computer Science.</p>

          <p>A familiar face came up during the lectures which was % or modulo. This was an operator that was often used in odd or even checkers.</p>
          <p>I was shocked to find out that modulo arithmetic was actually an example of a ring in abstract algebra. I thought that thing was just something that computers could do, like find the remainder after division.</p>
          <p>It turns out that modulo isn't just a tool in programming, but part of a world that helps us understand patterns, cycles, and structures. Learning about groups, rings & fields gave me a new appreciation for simple operations people use every day in Computer Science.</p>
          <!--ADD MORE CONTENT-->

        </div>
       </div>

        {:else if activeWindow === 'discrete-probability'}
      <!-- discrete probability window -->
       <div class="content-window">
        <div class="content-header">
          <h2>Discrete Probability</h2>
          <button on:click={closeWindow} class="close-button">X</button>
        </div>
        <div class="scrollable-content">
          <p>In CMSC 57, we talked about probability. The concepts allow us to help make decisions, if we were uncertain.</p>
          <p>When I think of a practical application of discrete probability, I think of <s>gambling</s> artificial intelligence, which is largely based on choosing random inputs that create the ideal output.</p>
          <p>It was fun seeing counting being applied again, despite there being a noticeable gap given by algebraic structures in between. Applying counting to probability opened up a lot of possibilities that would've taken forever to count by hand.</p>

          <!--ADD MORE CONTENT-->

        </div>
       </div>

        {:else if activeWindow === 'graphs'}
      <!-- graphs window -->
       <div class="content-window">
        <div class="content-header">
          <h2>Graphs</h2>
          <button on:click={closeWindow} class="close-button">X</button>
        </div>
        <div class="scrollable-content">

          <p>When my professor told us that this was one of her favorite
             Computer Science topic ever, <b>#felt</b>, to be honest. This was also one of my favorite topics in Computer Science.</p>
          <p>This topic was EVERYWHERE in Computer Science. Even outside it, graphs show up everywhere. Take Gantt charts in research writing, for example, they're basically digraphs that help visualize project schedules and dependencies.</p>
          <p>Artificial intelligence relies heavily on graphs. Neural networks are built upon weighted graphs, with multiple layers made with nodes (neurons) and edges, to achieve the ideal probability output.</p>
          <p>Without graphs, modern AI as we know it wouldn't be as possible.</p>
          <!--ADD MORE CONTENT-->

        </div>
       </div>
      {/if}
    </div>
  </div>
</main>

<style>

  .content-header button {
    background-color: #610000;
    border: none;
    cursor: pointer;
    font-size: 1.5rem;
    color: #fff;
    border-radius: 25%;
  }

  .content-header button:hover {
    background-color: #ff0000;
  }

  .content-header h2 {
    margin: 0;
    font-size: 3rem;
  }
  .content-window {
    height: 100%;
    display: flex;
    flex-direction: column;
    font-weight: 600;

  }

  .content-header{
    padding: 1rem;
    border-bottom: 1px solid #ccc;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
  }

  .scrollable-content {
    flex: 1;
    overflow-y: auto;
    padding: 1rem;
    font-size: 1.3rem;
  }

  .desktop-icon-container {
    cursor: pointer;
    transition: transform 0.2s;
  }

  .desktop-icon-container:hover {
    transform: scale(1.05);
  }

  b {
    font-weight: 1000; 
    text-decoration: underline;
  }

</style>
