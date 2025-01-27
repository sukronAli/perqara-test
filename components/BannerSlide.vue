<template>
  <section class="position-relative">
    <carousel
      :margin="30"
      :items="1"
      :stage-padding="650"
      :nav="false"
      loop
      class="carousel-banner"
      autoplay
    >
      <div v-for="(item, i) in listdata" :key="i" class="item-slider d-flex align-items-center">
        <img :src="require(`@/assets/images/${item.img}`)" alt="">
        <div class="caption-item">
          <div class="rate-caption-slider">
            <img src="@/assets/images/Star.svg" alt="">
            {{ item.rate }}
          </div>
          <h3>
            <nuxt-link :to="'/detail-movie/'+replaceName(item.title)">
              {{ item.title }}
            </nuxt-link>
          </h3>
          <div class="category-year mb-3">
            {{ item.tahun }} &#9679; {{ item.category }}
          </div>
          <p>
            {{ item.deskripsi }}
          </p>
        </div>
      </div>
    </carousel>
  </section>
</template>
<script lang="ts">
import { Component, Prop, Vue } from 'nuxt-property-decorator'
@Component
export default class BannerSlide extends Vue {
  @Prop() listdata!: { img: string, rate: number, title: string, tahun: number, category: string, deskripsi: string }[]
  replaceName (str:string) {
    str = str.replace(/\s+/g, '-').toLowerCase()
    return str
  }
}
</script>
