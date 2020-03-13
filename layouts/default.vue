<template>
  <div>
    <nav>
      <Logo/>
    </nav>
    <nuxt />
  </div>
</template>
<script>
import Logo from "~/components/Logo";
export default {
  components: {
    Logo
  }
}
</script>