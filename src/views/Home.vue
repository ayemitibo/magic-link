<script>

export default {
  name: 'App',
  mounted(){
     const plugin = document.createElement("script");
    plugin.setAttribute(
      "src",
      "https://auth.magic.link/pnp/login"
    );
    plugin.setAttribute(
      "data-magic-publishable-api-key",
      "pk_live_2C892575A2D828C6"
    );
    plugin.setAttribute(
      "data-redirect-uri",
      "/dashboard"
    );
    plugin.async = true;
    document.head.appendChild(plugin);
  }
}
</script>