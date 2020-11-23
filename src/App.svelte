<script>
    let phrase = "We all like dogs";
    let guess = "";
</script>

<svelte:head>
  <title>翻译者</title>
  <meta name="robots" content="noindex nofollow"/>
  <html lang="zh-CN"/>
</svelte:head>

<main>
  <h1>翻译句子</h1>
  <p>把下面的句子翻译为汉语</p>
  <p class="phrase">“{phrase}“</p>
  <p><input type="text" bind:value={guess} placeholder="翻译"></p>
  <p class="guess">{guess}</p>  
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: rgb(0, 102, 214);
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

    .phrase {
        font-style: italic;
    }

    .guess {
        color: rgb(0, 60, 70);
        font-size: 2em;
    }

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
