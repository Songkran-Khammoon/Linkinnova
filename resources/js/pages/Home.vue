<template>
  <section id="home">
    <v-container>
      <v-row class="mt-12 mb-6">
        <v-col lg="4" md="4" sm="6" cols="12">
          <v-card :class="{ 'on-hover': isHovering }" class="mx-auto style-shadow" height="auto" max-width="95%">
            <v-carousel hide-delimiters cycle hide-delimiter-background class="card-content" :show-arrows="false">
              <v-carousel-item disabled-3 v-for="(slide, i) in slides" :key="i" :src="app_url + img_naa[i]" cover>
              </v-carousel-item>
            </v-carousel>
            <v-card-text class="txt-content">
              {{ items[0].content }}
            </v-card-text>
            <div class="style-btn">
              <v-btn class="btn" variant="outlined" :href="items[0].path">
                see more
              </v-btn>
            </div>
          </v-card>
        </v-col>
        <v-col lg="4" md="4" sm="6" cols="12">
          <v-card :class="{ 'on-hover': isHovering }" class="mx-auto style-shadow" height="auto" max-width="95%">
            <v-carousel hide-delimiters cycle hide-delimiter-background class="card-content" :show-arrows="false">
              <v-carousel-item disabled-3 v-for="(slide, i) in slides" :key="i" :src="app_url + img_crp[i]" cover>
              </v-carousel-item>
            </v-carousel>
            <v-card-text class="txt-content">
              {{ items[1].content }}
            </v-card-text>
            <div class="style-btn">
              <v-btn class="btn" variant="outlined" :href="items[1].path">
                see more
              </v-btn>
            </div>
          </v-card>
        </v-col>
        <v-col lg="4" md="4" sm="6" cols="12">
          <v-card :class="{ 'on-hover': isHovering }" class="mx-auto style-shadow" height="auto" max-width="95%">
            <v-carousel hide-delimiters cycle hide-delimiter-background class="card-content" :show-arrows="false">
              <v-carousel-item disabled-3 v-for="(slide, i) in slides" :key="i" :src="app_url + img_cpp[i]" cover>
              </v-carousel-item>
            </v-carousel>
            <v-card-text class="txt-content">
              {{ items[2].content }}
            </v-card-text>
            <div class="style-btn">
              <v-btn class="btn" variant="outlined" :href="items[2].path">
                see more
              </v-btn>
            </div>
          </v-card>
        </v-col>
      </v-row>
      <div class="text-home-animetion">
        LINK INNOVA PROPERTIES COMPANY LIMITED 50 หมู่ 2 ตำบลตลาดขวัญ อำเภอดอยสะเก็ต
        จังหวัดเชียงใหม่ 50220 โทรศัพท์ : 053-039191 เบอร์มือถือ : 085-6956505
      </div>
    </v-container>
  </section>
</template>
<script>
export default {
  data: () => ({
    selectedItem: 0,
    items: [
      {
        content: "News and activities",
        img: "/images/img (1).jpg",
        path: "/News-and-activities",
      },
      {
        content: "Current projects",
        img: "/images/img (1).png",
        path: "/Current-projects",
      },
      {
        content: "Completed projects",
        img: "/images/img (2).jpg",
        path: "/Completed-projects",
      },
    ],
    slides: ["1", "2", "3"],
    img_naa: ["/images/img (1).jpg", "/images/img (1).png", "/images/img (2).jpg"],
    img_crp: ["/images/img (1).png", "/images/img (2).jpg", "/images/img (1).jpg"],
    img_cpp: ["/images/img (2).jpg", "/images/img (1).jpg", "/images/img (1).png"],
  }),
};
</script>
