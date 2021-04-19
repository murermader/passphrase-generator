<script>
  document.title = "Passphrase Generator";

  let wordCount = 4;
  let startsWithCapital = true;
  let appendNumber = true;
  let separationChar = "-";
  export let wordlist = [];

  let possibleWordCounts = [3, 4, 5, 6];

  function generatePassphrase() {
    console.log("Generate Passphrase");
  }
</script>

<main class="md:flex justify-center w-full p-8 box-border">
  <div>
    <h1 class="text-center">Passphrase Generator</h1>
    <div class="flex flex-col bg-gray-100 rounded-lg shadow-lg p-8 mt-4">
      <input type="text" class="mt-4" />
      <div class="grid grid-cols-2 grid-rows-4 mt-4 items-center">
        <label for="word-count">Words</label>
        <select bind:value={wordCount} id="word-count">
          {#each possibleWordCounts as wordCount (wordCount)}
            <option class={wordCount}>{wordCount}</option>
          {/each}
        </select>

        <label for="separation-char">Separation character</label>
        <input maxlength="1" type="text" bind:value={separationChar} />

        <label for="starts-with-capital">Starts with capital</label>
        <input
          bind:checked={startsWithCapital}
          type="checkbox"
          class="m-0 p-0"
        />

        <label for="starts-with-capital">Append number</label>
        <input bind:checked={appendNumber} type="checkbox" class="m-0 p-0" />
      </div>
      <button
        on:click={generatePassphrase}
        class="justify-self-end mt-4 bg-gray-50">New Password</button
      >
    </div>
  </div>

  <a class="absolute bottom-0 right-0 p-2 text-gray-500" href="#"
    >Datenschutzerklärung</a
  >
</main>
