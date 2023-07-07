<script>
    
    let names = ["Bruce", "Clark", "Diana", "Barry"];
    const shuffleNames = () => {
      names = shuffle(names);
    };
  </script>
  
  <style>
    main {
      font-family: sans-serif;
      text-align: center;
    }

	button{
		padding: 10px 30px;
		background-color: #444;
		border: 1px solid #444;
		color: #fff;
        margin-top: 10px;
	}
  </style>
  
  <main>
    {#each names as name (name)}
      <h2>{name}</h2>
      <input placeholder="Last name" />
    {/each}
    
    <div>
     <button on:click={shuffleNames}>Shuffle!</button>
    </div>
  </main>