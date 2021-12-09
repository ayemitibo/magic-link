<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>
<script>
export default {
  created(){
     const plugin = document.createElement("script");
    plugin.setAttribute(
      "src",
      "https://auth.magic.link/pnp/callback"
    );
    plugin.setAttribute(
      "data-magic-publishable-api-key",
      "pk_live_2C892575A2D828C6"
    );
    plugin.async = true;
    document.head.appendChild(plugin);
  },
  mounted(){
    window.addEventListener('@magic/ready', (event) => {
    const { magic, idToken, userMetadata, oauth } = event.detail;
    console.log(magic,idToken,userMetadata,oauth)
    // ...
  });
  }
}
</script>