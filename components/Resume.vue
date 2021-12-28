<template>
  <div id="resume">
    <a-row :gutter="30">
      <a-col :span="12">
        <div class="experienc">
          <div class="sub-heading">
            <h3>Experience</h3>
          </div>
          <ul class="experience-list">
            <li>
              <span class="left-line"></span>
              <div class="content">
                <h4>Senior Front-End Developer</h4>
                <h5>Cleverground Technology, Pune</h5>
                <p class="info">
                  Sit cupiditate praesentium ex esse nulla Facere fuga
                  perspiciatis eveniet provident neque Ea ratione non minus
                  temporibus ipsum Sunt minima
                </p>
              </div>
              <div class="year">
                <span class="to">Current</span>
                <span class="from">Aug 2021</span>
              </div>
            </li>
            <li>
              <span class="left-line"></span>
              <div class="content">
                <h4>Front-End Developer</h4>
                <h5>Formec Media LLP, Kolhapur</h5>
                <p class="info">
                  Sit cupiditate praesentium ex esse nulla Facere fuga
                  perspiciatis eveniet provident neque Ea ratione non minus
                  temporibus ipsum Sunt minima
                </p>
              </div>
              <div class="year">
                <span class="to">Aug 2021</span>
                <span class="from">Sep 2020</span>
              </div>
            </li>
          </ul>
        </div>
      </a-col>
      <a-col :span="12">
        <div class="sub-heading">
          <h3>Education</h3>
        </div>
        <div class="education-container">
          <div class="education" v-for="(item, i) in education" :key="i">
            <h4>{{ item.degree }}</h4>
            <p>{{ item.university }}</p>
            <span>{{ item.year }}</span>
          </div>
        </div>
        <div class="sub-heading">
          <h3>Skills</h3>
        </div>
        <div class="skills">
          <p>
            Html, Css, Scss, Javascript, vuejs, NuxtJs, ReactJs, NextJs,
            Graphql, Strapi, Nodejs, Express, Bootstrap, Tailwind, Antd,
            cypress, jest
          </p>
        </div>
      </a-col>
    </a-row>
  </div>
</template>

<script>
export default {
  name: "ResumeComponent",
  data() {
    return {
      education: [
        {
          degree: "BE - Bachelor of Engineering Computer Science",
          university: "Shivaji University, Kolhapur",
          year: 2019,
        },
        {
          degree: "Diploma - Computer Science",
          university: "MSBTE",
          year: 2016,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
#resume {
  position: relative;
  width: 100%;
  .experience-list {
    position: relative;
    margin: 0;
    padding: 0;
    list-style: none;
    li {
      position: relative;
      margin-left: 10px;
      padding: 20px;
      margin-bottom: 80px;
      &:last-child {
        margin-bottom: 0;
      }
      .left-line {
        width: 2px;
        height: 100%;
        background-color: $primary;
        left: -10px;
        top: 0;
        position: absolute;
        &::before {
          content: "";
          width: 10px;
          height: 10px;
          -webkit-border-radius: 50%;
          border-radius: 50%;
          border: 2px solid $primary;
          position: absolute;
          left: -4px;
          top: -10px;
        }
        &::after {
          content: "";
          width: 10px;
          height: 10px;
          -webkit-border-radius: 50%;
          border-radius: 50%;
          border: 2px solid $primary;
          position: absolute;
          left: -4px;
          bottom: -10px;
        }
      }
      .content {
        h4 {
          font-size: 18px;
          font-weight: 700;
          letter-spacing: 0.5px;
          line-height: 26px;
          margin: 0;
          text-transform: uppercase;
          color: $white;
        }
        h5 {
          margin-top: 5px;
          margin-bottom: 5px;
          font-size: 12px;
          font-family: "Roboto", sans-serif;
          font-weight: 600;
          text-transform: uppercase;
          color: $primary;
        }
        .info {
          font-size: 16px;
          margin-bottom: 0px;
          line-height: 1.65;
          color: $white;
        }
      }
      .year {
        height: 100%;
        left: -10px;
        top: 0;
        position: absolute;
        span {
          font-size: 16px;
          position: absolute;
          -webkit-transform: translateX(-120%);
          -ms-transform: translateX(-120%);
          transform: translateX(-120%);
          color: #ffffff;
        }
        .to {
          top: -18px;
        }
        .from {
          bottom: -18px;
        }
      }
    }
  }
  .education-container {
    margin-bottom: 50px;
    padding-top: 20px;
  }
  .education {
    margin-bottom: 20px;
    h4 {
      font-size: 16px;
      font-weight: 700;
      letter-spacing: 0.5px;
      line-height: 26px;
      margin: 0;
      text-transform: uppercase;
      color: $white;
    }
    p {
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 0.5px;
      line-height: 26px;
      margin: 0;
      text-transform: uppercase;
      color: $primary;
    }
    span {
      margin: 0;
      font-size: 12px;
      font-weight: 400;
      letter-spacing: 0.5px;
      line-height: 26px;
      margin: 0;
      text-transform: uppercase;
      color: $secondary-font;
    }
  }
  .skills {
    font-size: 18px;
    font-weight: 600;
    letter-spacing: 0.5px;
    line-height: 26px;
    margin: 0;
    text-transform: capitalize;
    color: $white;
  }
}
</style>