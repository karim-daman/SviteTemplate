<script>
  import { t, locale, locales } from "../locale/i18n";

  let isDropdownOpen = false;
  let selectedLanguage = "English";

  const toggleDropdown = () => {
    isDropdownOpen = !isDropdownOpen;
  };

  const handleButtonClick = (l) => {
    selectedLanguage = l;
    $locale = l;
    console.log(`Language changed: ${l}`);
    isDropdownOpen = false;
  };

  import { clickOutside } from "svelte-use-click-outside";

  function clickOutsideHandler() {
    isDropdownOpen = false;
  }
</script>

<div use:clickOutside={clickOutsideHandler} class=" dropdown absolute right-3">
  <button on:click={toggleDropdown} class="press flex w-full press px-2 rounded">
    <img src="flag_icons/{selectedLanguage}.svg" class="rounded-full w-5 p-0.5" alt="" />
  </button>
</div>

<div use:clickOutside={clickOutsideHandler} class=" dropdown absolute right-5">
  <div class={`dropdown-content ${isDropdownOpen ? "block" : "hidden"} bg-yellow-600 rounded-md w-[120px] m-0.5 mt-5 p-0.5`}>
    {#each locales as l}
      {#if l != selectedLanguage}
        <button on:click={() => handleButtonClick(l)} class="w-full hover:bg-black hover:rounded-md hover:text-white press flex px-2 py-0.5">
          <img src="flag_icons/{l}.svg" class="rounded-full w-4 mr-4" alt="" />
          <div class="text-xs">{l}</div>
        </button>
      {/if}
    {/each}
  </div>
</div>
