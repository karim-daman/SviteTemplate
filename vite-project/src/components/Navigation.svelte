<script>
  import ModalAuthentication from "./Modal_Authentication.svelte";
  import LanguageSelect from "$lib/LanguageSelect.svelte";
  import ThemeSelect from "$lib/ThemeSelect.svelte";
</script>

<nav class=" flex m-auto w-full h-16 border-b">
  <div class="w-1/6 content-center flex items-center justify-center">
    <!-- <img src="logo.png" class="h-10" alt="" /> -->
    Logo
  </div>
  <div class="flex-auto">
    <div class="flex h-full items-center justify-center">
      <a href="#" class="flex-auto hover:underline hover:text-blue-600 flex items-center justify-center">Home</a>
      <a href="#" class="flex-auto hover:underline hover:text-blue-600 flex items-center justify-center">About</a>
      <a href="#" class="flex-auto hover:underline hover:text-blue-600 flex items-center justify-center">Projects</a>
      <a href="#" class="flex-auto hover:underline hover:text-blue-600 flex items-center justify-center">Contact</a>
      <a href="#" class="flex-auto hover:underline hover:text-blue-600 flex items-center justify-center">Pricing</a>
    </div>
  </div>
  <ModalAuthentication />
</nav>
<nav class="h-8 bg-slate-200 w-full flex flex-row-reverse pr-4">
  <LanguageSelect />
  <ThemeSelect />
</nav>
