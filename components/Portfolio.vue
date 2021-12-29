<template>
  <div class="portfolio-work">
    <div class="sub-heading">
      <h3>My Recent Work</h3>
      <div class="card-container">
        <div
          v-for="(item, i) in workData"
          :key="i"
          class="card"
          @mouseenter="(hover = true), (hoverIndex = i)"
          @mouseleave="(hover = false), (hoverIndex = false)"
        >
          <img
            :src="item.image"
            alt=""
            :style="
              hover && hoverIndex == i
                ? { transform: 'scale(1.2)' }
                : { transform: 'scale(1)' }
            "
          />
          <transition name="fade">
            <div v-if="hover && hoverIndex == i" class="overlay">
              <h4>{{ item.desc }}</h4>
              <a :href="item.link" target="_blank"
                >Visit Website <a-icon class="right-icon" type="right"
              /></a>
            </div>
          </transition>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PortfolioComponent",
  data() {
    return {
      hoverIndex: false,
      hover: false,
      workData: [
        {
          image: "/cg.webp",
          desc: "CleverGround LMS is designed and curated to suit the digital needs of modern colleges and university. Bringing the exact combination of automated teaching and learning experience.",
          link: "https://product.cleverground.com/",
        },
        {
          image: "/netaji.png",
          desc: "Netaji Safe Company Is A Reputed And Trusted Name Which Stands For Quality, Durability, Reliability And Affordability. Netaji Safe Company Offers A Complete Range Of Security Equipment",
          link: "https://www.netajisafe.com/",
        },
        {
          image: "/balaji.png",
          desc: "Balaji Villa is one of the famous luxurious 4 bedrooms bunglow in Panhala, Kolhapur.",
          link: "https://balajivillapanhala.com/",
        },
        {
          image: "/barai.png",
          desc: "Dr. Barai clinic is a Sex and Skin Care Centre. specialises in Acne, Acne Scars, skin whitening, Skin Tan, hair Treatment,   Tattoo removal, Hair Reduction, hair Transplant,  sexual disorder. ",
          link: "https://admin.drbaraisclinic.com/",
        },
        {
          image: "/cachetan.png",
          desc: "Chetan Oswal & Associates (COA) is a TEAM of young and dynamic professionals with a passion to provide personalized, practical and innovative solutions to complex tax problems.",
          link: "https://cachetanoswal.com/",
        },
        {
          image: "/dental.png",
          desc: " The speciality dental clinic is in kolhapur. Detailed Examination, discussion of various treatment modalities with diagnostic models, photographs.",
          link: "https://www.thespecialitydental.com/",
        },
        {
          image: "/malati.png",
          desc: "Malati Autocast Pvt. Ltd. is the newest addition to the Malati Group and lives up to the 50 year heritage symbolizing Quality and Trust.",
          link: "https://malatiautocast.com/",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.portfolio-work {
  position: relative;
  width: 100%;
  .card-container {
    position: relative;
    display: grid;
    grid-template-columns: auto auto auto;
    gap: 30px;
    margin-top: 40px;
    .card {
      position: relative;
      background-color: $white;
      width: 100%;
      height: 220px;
      border-radius: 10px;
      transition: 0.2s ease all;
      overflow: hidden;
      .overlay {
        position: absolute;
        width: 100%;
        height: 100%;
        background-color: #141c3a;
        right: 0;
        top: 0;
        opacity: 0.99;
        transition: 0.2s ease all;
        padding: 25px 15px;
        display: flex;
        flex-direction: column;
        // justify-content: center;
        align-items: center;
        h4 {
          color: $white;
          font-size: 16px;
          font-weight: 500;
          text-align: center;
        }
        a {
          position: absolute;
          bottom: 15px;
          border: 2px solid $primary;
          padding: 10px 30px;
          border-radius: 30px;
          color: $white;
          font-size: 14px;
          font-weight: 500;
          transition: 0.3s ease all;
          cursor: pointer;
          .right-icon {
            font-size: 16px;
            font-weight: 600;
          }
          &:hover {
            background: $primary;
          }
        }
      }
      img {
        width: 100%;
        height: 100%;
        object-fit: contain;
        transition: 0.3s ease all;
      }
    }
  }
}

.fade-enter,
.fade-leave-to {
  transform: translateY(120%);
}
</style>