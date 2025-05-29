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
      <p>alex cmsc 57 ePortfolio yayayay !!</p>
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

          <p>Content for Counting goes here...</p>
          <!--ADD MORE CONTENT-->

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

          <p>Content for Algebraic Structures and Groups goes here...</p>
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

          <p>Content for Groups, Rings, & Fields goes here...</p>
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

          <p>Content for Discrete Probability goes here...</p>
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

          <p>Content for Graphs goes here...</p>
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
  .content-window {
    height: 100%;
    display: flex;
    flex-direction: column;

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
  }

  .desktop-icon-container {
    cursor: pointer;
    transition: transform 0.2s;
  }

  .desktop-icon-container:hover {
    transform: scale(1.05);
  }
</style>
