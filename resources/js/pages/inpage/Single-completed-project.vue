<template>
  <section class="page-contents">
    <div class="mx-auto opacity-banner">
      <v-img dark :src="app_url + '/images/banner/banner-completed-projects.jpg'" class="banner-inpage align-center"
        max-height="500">
        <v-row>
          <v-col class="text-center" cols="12">
            <span class="underline-header text-white">Completed project</span>
          </v-col>
        </v-row>
      </v-img>
    </div>
    <div class="header-page">
      <ol>
        <li>
          <router-link to="/"><strong>Home</strong></router-link>
        </li>
        <li>
          <v-icon>mdi-chevron-right</v-icon>
        </li>
        <li>
          <router-link to="/Current-projects"><strong>ALL Current Projects</strong></router-link>
        </li>
        <li>
          <v-icon>mdi-chevron-right</v-icon>
        </li>
        <li>{{ post.subtitle }}</li>
      </ol>
    </div>
    <div class="single-content">
      <v-container v-if="post.video != ''">
        <div class="video">
          <v-row class="mb-3">
            <v-col cols="12" sm="12" md="6" lg="6">
              <div class="videoWrapper">
                <embed :src="post.video" type="" />
              </div>
            </v-col>
            <v-col cols="12" sm="12" md="6" lg="6">
              <h2>{{ post.title }}</h2>
              <h5>{{ post.subtitle }}</h5>
            </v-col>
          </v-row>
        </div>
      </v-container>
      <div class="gallery">
        <v-row>
          <v-col cols="6" sm="4" md="3" lg="2" v-for="(item, index) in items" :key="index" class="card-content">
            <v-card class="mx-auto" height="95%" v-bind="props">
              <div class="class-image">
                <v-img height="150" :src="app_url + item.img" cover />
              </div>
            </v-card>
          </v-col>
        </v-row>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    id: {
      require: true,
      type: Number,
      default: false,
    },
  },
  data: () => ({
    // page: 1,
    // selectedItem: 0,
    items: [
      {
        id: 1,
        title: "LINK อาคารบูรณาการ ๗ ชั้น โรงพยาบาลหลังสวน , จังหวัดชุมพร , มกราคม ๒๕๖๔",
        subtitle:
          "โครงการก่อสร้างอาคารอำนวยการผู้ป่วยนอก และอุบัติเหตุฉุกเฉิน 11 ชั้น โรงพยาบาลราชบุรี",
        img: "/images/images-completed-project/img (1).png",
        video: "https://www.youtube.com/embed/4ML8VJI6Zo8",
      },
      {
        id: 2,
        title: "LINK อาคารบูรณาการ ๗ ชั้น โรงพยาบาลหลังสวน , จังหวัดชุมพร , มกราคม ๒๕๖๔",
        subtitle: "โครงการก่อสร้างท่าอากาศยานเบตง",
        img: "/images/images-completed-project/img (2).png",
        video: "https://www.youtube.com/embed/4ML8VJI6Zo8",
      },
      {
        id: 3,
        title: "LINK อาคารบูรณาการ ๗ ชั้น โรงพยาบาลหลังสวน , จังหวัดชุมพร , มกราคม ๒๕๖๔",
        subtitle: "โครงก่อสร้างคอนโด Hiltania",
        img: "/images/images-completed-project/img (3).png",
        video: "",
      },
      {
        id: 4,
        title: "LINK อาคารบูรณาการ ๗ ชั้น โรงพยาบาลหลังสวน , จังหวัดชุมพร , มกราคม ๒๕๖๔",
        subtitle: "โครงก่อสร้างบ้านพักศาลปกครองเชียงใหม่",
        img: "/images/images-completed-project/img (4).png",
        video: "https://www.youtube.com/embed/4ML8VJI6Zo8",
      },
      {
        id: 5,
        title: "LINK อาคารบูรณาการ ๗ ชั้น โรงพยาบาลหลังสวน , จังหวัดชุมพร , มกราคม ๒๕๖๔",
        subtitle: "โครงก่อสร้างอาคารเรียนและปฏิบัติการรวม คณะมนุษยศาสตร์",
        img: "/images/images-completed-project/img (5).png",
        video: "",
      },
      {
        id: 6,
        title: "LINK อาคารบูรณาการ ๗ ชั้น โรงพยาบาลหลังสวน , จังหวัดชุมพร , มกราคม ๒๕๖๔",
        subtitle: "โครงก่อสร้างอาคารที่ทำการศาล จังหวัดกระบี่",
        img: "/images/images-completed-project/img (6).png",
        video: "",
      },
      {
        id: 7,
        title: "LINK อาคารบูรณาการ ๗ ชั้น โรงพยาบาลหลังสวน , จังหวัดชุมพร , มกราคม ๒๕๖๔",
        subtitle:
          "โครงการก่อสร้างอาคารอำนวยการผู้ป่วยนอก และอุบัติเหตุฉุกเฉิน 11 ชั้น โรงพยาบาลราชบุรี",
        img: "/images/images-completed-project/img (1).png",
        video: "https://www.youtube.com/embed/4ML8VJI6Zo8",
      },
      {
        id: 8,
        title: "LINK อาคารบูรณาการ ๗ ชั้น โรงพยาบาลหลังสวน , จังหวัดชุมพร , มกราคม ๒๕๖๔",
        subtitle: "โครงการก่อสร้างท่าอากาศยานเบตง",
        img: "/images/images-completed-project/img (2).png",
        video: "https://www.youtube.com/embed/4ML8VJI6Zo8",
      },
      {
        id: 9,
        title: "LINK อาคารบูรณาการ ๗ ชั้น โรงพยาบาลหลังสวน , จังหวัดชุมพร , มกราคม ๒๕๖๔",
        subtitle: "โครงก่อสร้างคอนโด Hiltania",
        img: "/images/images-completed-project/img (3).png",
        video: "",
      },
      {
        id: 10,
        title: "LINK อาคารบูรณาการ ๗ ชั้น โรงพยาบาลหลังสวน , จังหวัดชุมพร , มกราคม ๒๕๖๔",
        subtitle: "โครงก่อสร้างบ้านพักศาลปกครองเชียงใหม่",
        img: "/images/images-completed-project/img (4).png",
        video: "https://www.youtube.com/embed/4ML8VJI6Zo8",
      },
      {
        id: 11,
        title: "LINK อาคารบูรณาการ ๗ ชั้น โรงพยาบาลหลังสวน , จังหวัดชุมพร , มกราคม ๒๕๖๔",
        subtitle: "โครงก่อสร้างอาคารเรียนและปฏิบัติการรวม คณะมนุษยศาสตร์",
        img: "/images/images-completed-project/img (5).png",
        video: "",
      },
      {
        id: 12,
        title: "LINK อาคารบูรณาการ ๗ ชั้น โรงพยาบาลหลังสวน , จังหวัดชุมพร , มกราคม ๒๕๖๔",
        subtitle: "โครงก่อสร้างอาคารที่ทำการศาล จังหวัดกระบี่",
        img: "/images/images-completed-project/img (6).png",
        video: "",
      },
    ],
  }),
  computed: {
    post() {
      return this.items.find((post) => post.id === Number(this.id));
    },
  },
};
</script>
