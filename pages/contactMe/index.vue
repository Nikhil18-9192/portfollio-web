<template>
  <div>
    <div id="contact">
      <PageHeading title="Contact Me" />
      <ContactForm />
    </div>
    <div class="map">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d625.4809220956398!2d74.19916346499649!3d16.700576671418037!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bc1abde216e8e0d%3A0xa700e77417808ff!2sKorane%20steel!5e0!3m2!1sen!2sin!4v1640664662335!5m2!1sen!2sin"
        width="100%"
        height="250"
        style="border: 0"
        allowfullscreen=""
        loading="lazy"
      ></iframe>
    </div>
  </div>
</template>

<script>
export default {
  layout: "default",
};
</script>
<style lang="scss" scoped>
#contact {
  position: relative;
  max-width: 1040px;
  width: 90%;
  margin: 0 auto;
  height: 100%;
  min-height: 100vh;
}
</style>