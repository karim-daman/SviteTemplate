<script>
  import { t, locale, locales } from "../locale/i18n";
  import { onMount } from "svelte";

  let isDropdownOpen = false;
  let selectedLanguage = "English";

  const toggleDropdown = () => {
    isDropdownOpen = !isDropdownOpen;
  };

  const handleButtonClick = (l) => {
    selectedLanguage = l;
    $locale = l;
    localStorage.setItem("selectedLanguage", l); // Save selected language to local storage
    isDropdownOpen = false;
  };

  import { clickOutside } from "svelte-use-click-outside";

  function clickOutsideHandler() {
    isDropdownOpen = false;
  }

  // Load selected language from local storage on component mount
  onMount(() => {
    const storedLanguage = localStorage.getItem("selectedLanguage");
    if (storedLanguage && locales.includes(storedLanguage)) {
      selectedLanguage = storedLanguage;
      $locale = storedLanguage;
    }
  });
</script>

<div use:clickOutside={clickOutsideHandler} class="dropdown absolute right-3">
  <button on:click={toggleDropdown} class="press flex w-full press px-2 rounded">
    <img src={`flag_icons/${selectedLanguage}.svg`} class="rounded-full w-5 p-0.5" alt="" />
  </button>
</div>

<div use:clickOutside={clickOutsideHandler} class="dropdown absolute right-5">
  <div class={`dropdown-content ${isDropdownOpen ? "block" : "hidden"}  bg-yellow-500 rounded-md w-[120px] mx-0.5 mt-6 p-0.5`}>
    {#each locales as l}
      {#if l != selectedLanguage}
        <button on:click={() => handleButtonClick(l)} class="w-full hover:bg-black hover:rounded-md hover:text-white press flex px-2 py-0.5">
          <img src={`flag_icons/${l}.svg`} class="rounded-full w-4 mr-4" alt="" />
          <div class="text-xs text-white">{l}</div>
        </button>
      {/if}
    {/each}
  </div>
</div>
