<script>
  import { t as translation } from "../locale/i18n";
</script>

<!-- <div class="absolute right-7"><LanguageSelect /></div> -->

<h1 class="p-5 m-5 bg-black rounded-md text-white">
  {@html $translation("greeting")} your site is live! <br />
  <p class="text-xs">{@html $translation("message")}</p>
  <br />
</h1>
