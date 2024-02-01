<script>
  import LanguageSelect from "$lib/LanguageSelect.svelte";

  let avatarDropDownOpen = false;
</script>

<nav class=" flex w-full h-16">
  <div class="w-1/6 content-center flex items-center justify-center">
    <img src="CompanyLogo.png" class="h-10 rounded-full" alt="" />
  </div>
  <div class="flex-auto">
    <div class="flex h-full items-center justify-center">
      <div class="flex-auto underline flex items-center justify-center">link</div>
      <div class="flex-auto underline flex items-center justify-center">link</div>
      <div class="flex-auto underline flex items-center justify-center">link</div>
      <div class="flex-auto underline flex items-center justify-center">link</div>
      <div class="flex-auto underline flex items-center justify-center">link</div>
    </div>
  </div>
  <button
    on:click={() => {
      avatarDropDownOpen = !avatarDropDownOpen;
    }}
    class="w-1/6 flex items-center justify-center press">
    <img src="flag_icons/jp.svg" class="h-10 rounded-full" alt="" />
    <div
      id="dropdownAvatarName"
      class="absolute {avatarDropDownOpen ? 'block' : 'hidden'} top-16 right-5 z-10 bg-white divide-y divide-gray-100 rounded-lg shadow w-44 dark:bg-gray-700 dark:divide-gray-600">
      <div class="px-4 py-3 text-sm text-gray-900 dark:text-white">
        <div class="font-medium">Pro User</div>
        <div class="truncate">name@company.com</div>
      </div>
      <ul class="py-2 text-sm text-gray-700 dark:text-gray-200" aria-labelledby="dropdownInformdropdownAvatarNameButtonationButton">
        <li>
          <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Dashboard</a>
        </li>
        <li>
          <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Settings</a>
        </li>
        <li>
          <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Earnings</a>
        </li>
      </ul>
      <div class="py-2">
        <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 dark:hover:bg-gray-600 dark:text-gray-200 dark:hover:text-white">Sign out</a>
      </div>
    </div>
  </button>

  <LanguageSelect />
</nav>
