<script>
</script>

<main class="md:flex sm:w-full">
  <div>
    <h1 class="text-center">Passphrase Generator</h1>
    <div class="flex flex-col bg-gray-100 rounded-lg shadow-lg p-8 mt-4">
      <input type="text" class="mt-4" />
      <div class="grid grid-cols-2 grid-rows-4 mt-6">
        <label for="word-count">Words</label>
        <select name="" id="word-count">
          <option value="3" />
          <option value="4" />
          <option value="5" />
          <option value="6" />
        </select>

        <div>3</div>
      </div>
      <button class="justify-self-end mt-4 bg-gray-50">Generate</button>
    </div>
  </div>
</main>

<style global lang="postcss">
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
</style>
