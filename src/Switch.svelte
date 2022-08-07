<script>
  export let isChecked = false;
  export let id = "";

  // Von hier geklaut: https://css-tricks.com/the-checkbox-hack/
</script>

<main>
  <div>
    <input bind:checked={isChecked} {id} type="checkbox" />
    <label for={id}>Switch</label>
  </div>
</main>

<style>
  div {
    position: relative;
    display: inline-block;
  }

  input {
    display: none;
  }

  label {
    display: block;
    width: 48px;
    height: 24px;
    text-indent: -150%;
    clip: rect(0 0 0 0);
    color: transparent;
    user-select: none;
  }

  label::before,
  label::after {
    content: "";
    display: block;
    position: absolute;
    cursor: pointer;
  }

  label::before {
    width: 100%;
    height: 100%;
    background-color: #dedede;
    border-radius: 9999em;
    -webkit-transition: background-color 0.25s ease;
    transition: background-color 0.25s ease;
  }

  @media (prefers-color-scheme: dark) {
    label::before {
      background-color: #292A28;
      border: 1px solid black;
    }
  }

  label::after {
    top: 0;
    left: 0;
    width: 24px;
    height: 24px;
    border-radius: 50%;
    background-color: #fff;
    box-shadow: 0 0 2px rgba(0, 0, 0, 0.45);
    -webkit-transition: left 0.25s ease;
    transition: left 0.25s ease;
  }

  @media (prefers-color-scheme: dark) {
    label::after {
      background-color: #EEEEED;
    }
  }

  /* Diese 2 Regeln sind komisch: https://css-tricks.com/almanac/selectors/c/checked/ */
  input[type="checkbox"]:checked + label::before {
    background-color: #236bd7;
  }
  input[type="checkbox"]:checked + label::after {
    left: 24px;
  }

  main {
    text-align: left;
  }
</style>
