<template>
  <b-card no-body class="card-movie">
    <img class="img-cover-movie mb-3" :src="require(`@/assets/images/${img}`)" alt="">
    <div class="pita-movie">
      {{ rate }}
    </div>
    <div class="title-movie">
      <div class="nama">
        {{ title }}
      </div>
      <div class="tahun">
        {{ tahun }}
      </div>
    </div>
    <div class="box-hover">
      <div>
        <div class="rate-view d-flex align-items-center justify-content-center mb-4">
          <img src="@/assets/images/Star.svg" class="mr-2" alt="">
          {{ rate }}
        </div>
        <div class="category-movie text-center mb-4">
          Action
        </div>
        <div class="d-flex justify-content-center">
          <nuxt-link :to="'/detail-movie/'+url" class="btn-link">
            VIEW
          </nuxt-link>
        </div>
      </div>
    </div>
  </b-card>
</template>
<script lang="ts">
import { Component, Prop, Vue } from 'nuxt-property-decorator'
@Component
export default class ProductMovie extends Vue {
  @Prop() img!: string
  @Prop() title!: string
  @Prop() tahun!: string
  @Prop() rate!: string
  @Prop() url!: string
}
</script>
