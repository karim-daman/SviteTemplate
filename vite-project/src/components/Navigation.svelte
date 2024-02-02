<script>
  import ModalAuthentication from "./Modal_Authentication.svelte";
  import LanguageSelect from "$lib/LanguageSelect.svelte";
  import ThemeSelect from "$lib/ThemeSelect.svelte";
  import { isDarkTheme } from "$stores/AppStore";
</script>

<nav class=" flex m-auto w-full h-16">
  <div class="w-1/6 content-center flex items-center justify-center">
    <!-- <img src="logo.png" class="h-10" alt="" /> -->
    Logo
  </div>
  <div class="flex-auto">
    <div class="flex h-full items-center justify-center">
      <a href="#" class=" mx-1 flex-auto press hover:text-blue-600 flex items-center justify-center">Home</a>
      <a href="#" class=" mx-1 flex-auto press hover:text-blue-600 flex items-center justify-center">About</a>
      <a href="#" class=" mx-1 flex-auto press hover:text-blue-600 flex items-center justify-center">Projects</a>
      <a href="#" class=" mx-1 flex-auto press hover:text-blue-600 flex items-center justify-center">Contact</a>
      <a href="#" class=" mx-1 flex-auto press hover:text-blue-600 flex items-center justify-center">Pricing</a>
    </div>
  </div>
  <ModalAuthentication />
</nav>
<nav class="h-8 {$isDarkTheme ? 'bg-[#282727]' : 'bg-slate-100'}  w-full flex flex-row-reverse pr-4">
  <LanguageSelect />
  <ThemeSelect />
</nav>
