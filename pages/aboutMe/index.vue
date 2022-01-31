<template>
  <div id="about">
    <PageHeading title="About Me" />
    <div>
      <a-row class="about-info" :gutter="30">
        <a-col :span="15">
          <h3>Front-end Web Developer</h3>
          <p>
            Passionate Front end web developer having 1.5+ years experience in
            ReactJs, vueJs framework and converting designs into appealing
            experiences using html5, scss to end users which are pixel perfect.
            Good Knowledge of UI Design Principles. Can build user interfaces
            which are not only visually attractive but also usable and
            accessible across multiple devices providing seamless experience to
            user.
          </p>
          <!-- <p>
            Consectetur consectetur nesciunt nesciunt blanditiis amet? Quod quis
            unde aliquid excepturi laudantium? Illo architecto aliquam velit
            illo magnam neque perferendis sint Incidunt eius ipsa inventore
            labore eos velit. Minus hic magni reiciendis necessitatibus ex
            Quidem officia deleniti accusamus obcaecati dolores. Porro culpa
            quibusdam impedit porro praesentium excepturi. Alias ab consequatur?
          </p> -->
        </a-col>
        <a-col :span="9">
          <h3>Personal Information</h3>
          <div class="info">
            <p><span>Name</span> : Nikhil Korane</p>
            <p><span>Age</span> : 27 years</p>
            <p><span>Residence</span> : Kolhapur, India</p>
            <p><span>Address</span> : 1352, A ward, Laxtirth, 416010</p>
            <P
              ><span>Email</span> :
              <a href="mailto:nikhilkorane08@gmail.com" rel="noreferrer"
                >nikhilkorane08@gmail.com</a
              ></P
            >
            <p>
              <span>Phone</span> :
              <a href="tel:9595756168" rel="noreferrer">9595756168</a>
            </p>
          </div>
          <a
            class="resume-btn"
            href="/React_Developer_Deepak.pdf"
            rel="noreferrer"
            target="_blank"
            download
          >
            <div class="overlay"></div>
            Download Resume</a
          >
        </a-col>
      </a-row>
      <a-row class="services" :gutter="30">
        <div class="sub-heading">
          <h3>Services</h3>
        </div>
        <a-col :span="6">
          <div class="service-card">
            <a-icon class="service-icon" type="laptop" />
            <h4>Web Development</h4>
            <p>
              Amet aspernatur delectus maxime ducimus similique Ratione
              asperiores corporis provident aut libero.
            </p>
          </div>
        </a-col>
        <a-col :span="6">
          <div class="service-card">
            <a-icon class="service-icon" type="eye" />
            <h4>Web Design</h4>
            <p>
              Amet aspernatur delectus maxime ducimus similique Ratione
              asperiores corporis provident aut libero.
            </p>
          </div>
        </a-col>
        <a-col :span="6">
          <div class="service-card">
            <a-icon class="service-icon" type="api" />
            <h4>Api Integration</h4>
            <p>
              Amet aspernatur delectus maxime ducimus similique Ratione
              asperiores corporis provident aut libero.
            </p>
          </div>
        </a-col>
        <a-col :span="6">
          <div class="service-card">
            <a-icon class="service-icon" type="mobile" />
            <h4>Responsive Design</h4>
            <p>
              Amet aspernatur delectus maxime ducimus similique Ratione
              asperiores corporis provident aut libero.
            </p>
          </div>
        </a-col>
      </a-row>
    </div>
  </div>
</template>

<script>
export default {
  layout: "default",
};
</script>
<style lang="scss" scoped>
#about {
  position: relative;
  max-width: 1040px;
  width: 90%;
  margin: 0 auto;
  height: 100%;
  min-height: 100vh;
  margin-bottom: 100px;
  .about-info {
    margin-bottom: 70px;
    h3 {
      position: relative;
      font-size: 22px;
      font-weight: 700;
      color: $white;
      margin-bottom: 20px;
    }
    .info {
      padding-bottom: 20px;
    }
    p {
      font-size: 16px;
      color: $white;
      line-height: 1.65;
      font-weight: 500;
      margin-bottom: 16px;

      span {
        padding-bottom: 1px;
        border-bottom: 2px solid $primary;
      }
      a {
        text-decoration: none;
        color: $white;
      }
    }
  }
  .services {
    .service-card {
      color: $white;
      display: flex;
      flex-direction: column;
      align-items: center;
      .service-icon {
        font-size: 50px;
        margin-bottom: 10px;
        line-height: 1em;
        color: $primary;
      }
      h4 {
        font-size: 18px;
        font-weight: 600;
        color: $white;
        font-family: "Playfair Display", serif;
      }
      p {
        font-size: 14.5px;
        line-height: 22px;
        margin-top: 15px;
        margin-bottom: 15px;
        max-width: 237px;
        margin: 0 auto;
        text-align: center;
      }
    }
  }
}
</style>
