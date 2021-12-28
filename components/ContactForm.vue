<template>
  <div id="contact-form">
    <div class="sub-heading">
      <h3>Lets Talk</h3>
    </div>
    <div class="form">
      <a-row :gutter="[30, 50]">
        <a-col :span="12">
          <a-input placeholder="Name" @change="test" />
        </a-col>
        <a-col :span="12">
          <a-input placeholder="Email" />
        </a-col>
        <a-col :span="24">
          <a-textarea placeholder="Message" />
        </a-col>
        <a-col :span="24">
          <a class="resume-btn" href="#">
            <div class="overlay"></div>
            Send Message</a
          >
        </a-col>
      </a-row>
    </div>
    <a-row class="contact-info">
      <a-col :span="8">
        <a-icon class="contact-icon" type="aliwangwang" theme="filled" />
        <a href="mailto:nikhilkorane08@gmail.com"
          ><span>nikhilkorane08@gmail.com</span>
        </a>
      </a-col>
      <a-col :span="8">
        <a-icon class="contact-icon" type="environment" theme="filled" />
        <span>1352, A ward, kolhapur</span>
      </a-col>
      <a-col :span="8">
        <a-icon class="contact-icon" type="phone" theme="filled" />
        <a href="tel:9595756168"><span>9595756168</span></a>
      </a-col>
    </a-row>
  </div>
</template>

<script>
export default {
  name: "ContactForm",
  methods: {
    test() {
      console.log("test");
    },
  },
};
</script>

<style lang="scss" scoped>
#contact-form {
  position: relative;
  width: 100%;
  .form {
    width: 70%;
    margin: 0 auto;

    .ant-col {
      text-align: center;
    }
    input {
      width: 100%;
      border-radius: 0;
      border: 2px solid #999;
      height: 40px;
      transition: all 0.5s ease;
      position: relative;
      background-color: transparent;
      color: $white;
      font-size: 16px;
      &::placeholder {
        color: $white;
        font-weight: 500;
        font-size: 18px;
      }
    }
    textarea {
      width: 100%;
      border-radius: 0;
      border: 2px solid #999;
      transition: all 0.5s ease;
      height: 146px;
      position: relative;
      background-color: transparent;
      color: $white;
      font-size: 16px;
      &::placeholder {
        color: $white;
        font-weight: 500;
        font-size: 18px;
      }
    }
  }
  .contact-info {
    text-align: center;
    padding-top: 70px;
    .ant-col {
      display: flex;
      flex-direction: column;
      .contact-icon {
        font-size: 36px;
        line-height: 1em;
        color: $primary;
        margin-bottom: 8px;
      }
      a {
        text-decoration: none;
        color: $white;
        font-size: 18px;
        font-family: "Playfair Display", serif;
        font-weight: 600;
      }
      span {
        color: $white;
        font-size: 18px;
        font-family: "Playfair Display", serif;
        font-weight: 600;
      }
    }
  }
}
</style>