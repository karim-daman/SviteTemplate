<script>
  import Router from "svelte-spa-router";
  import routes from "./routes";
  import Navbar from "$components/Navigation.svelte";
</script>

<Navbar />

<main>
  <Router {routes} />
</main>
