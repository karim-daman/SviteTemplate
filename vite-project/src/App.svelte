<script>
  import Router from "svelte-spa-router";
  import routes from "./routes";
  import Navbar from "$components/Navigation.svelte";
  import Footer from "$components/Footer.svelte";
</script>

<Navbar />

<main>
  <Router {routes} />
</main>

<Footer />
