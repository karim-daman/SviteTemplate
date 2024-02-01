<script>
  import { onMount } from "svelte";
  import { t } from "../locale/i18n";
  import LanguageSelect from "$lib/LanguageSelect.svelte";

  import ThemeSelect from "$lib/ThemeSelect.svelte";
</script>

<LanguageSelect />

<h1 class="p-5 m-5 bg-black rounded-md text-white">
  {@html $t("greeting")} your site is live! <br />
  <p class="text-xs">{@html $t("message")}</p>
  <br />
  <ThemeSelect />
</h1>
