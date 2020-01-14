<template>
  <div>
    <AboutTimeline />
    <AboutQrcode />
  </div>
</template>

<script>
import AboutQrcode from "~/components/AboutQrcode.vue";
import AboutTimeline from "~/components/AboutTimeline.vue";

export default {
  components: {
    AboutQrcode,
    AboutTimeline
  }
};
</script>

<style scoped></style>
