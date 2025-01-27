<template>
  <section>
    <section class="bg-dark-gray section-banner pb-5">
      <BannerSlide :listdata="listSlider" />
    </section>
    <section class="bg-dark-gray pb-5">
      <div class="bg-gray box-backdrop" />
      <div class="box-content">
        <b-container>
          <b-row class="mb-5">
            <b-col md="6">
              <div class="title-section">
                <div class="pita" />
                <h4>Discover Movie</h4>
              </div>
            </b-col>
            <b-col md="6" class="d-flex align-items-center">
              <div class="box-switch d-flex align-items-center justify-content-end">
                <label v-for="(item, i) in listSort" :key="i" class="container-check d-flex align-items-center mb-0 pl-0 pr-2">
                  <input
                    v-model="sort"
                    type="radio"
                    name="sort"
                    :value="item.value"
                  >
                  <span class="checkmark-button">{{ item.label }}</span>
                </label>
              </div>
            </b-col>
          </b-row>
          <section v-if="sort === 'STR01'">
            <div class="row d-flex justify-content-center">
              <div v-for="(item, i) in movie" :key="i" class="col-md-5ths px-3 mb-4">
                <ProductMovie :img="item.img" :title="item.title" :tahun="item.tahun" :rate="item.rate" :url="replaceName(item.title)" />
              </div>
            </div>
          </section>
          <section v-else>
            <div class="row d-flex justify-content-center">
              <div v-for="(item, i) in movie" :key="i" class="col-md-5ths px-3 mb-4">
                <ProductMovie :img="item.img" :title="item.title" :tahun="item.tahun" :rate="item.rate" :url="replaceName(item.title)" />
              </div>
            </div>
          </section>
        </b-container>
      </div>
    </section>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
@Component
export default class IndexPage extends Vue {
  // name: 'IndexPage',
  data () {
    return {
      sort: 'STR01',
      listSort: [
        {
          id: '1',
          value: 'STR01',
          label: 'Popularity'
        },
        {
          id: '2',
          value: 'STR02',
          label: 'Release Date'
        }
      ],
      listSlider: [
        {
          id: '1',
          title: 'News of the World',
          tahun: '2020',
          img: 'banner1.png',
          rate: '7.0',
          category: 'Drama',
          deskripsi: 'A Texan traveling across the wild West bringing the news of the world to local townspeople, agrees to help rescue a young girl who was kidnapped.'
        },
        {
          id: '2',
          title: 'Space Sweepers',
          tahun: '2021',
          img: 'banner2.png',
          rate: '6.4',
          category: 'Sci-Fi',
          deskripsi: 'When the crew of a space junk collector ship called The Victory discovers a humanoid robot named Dorothy that`s known to be a weapon of mass destruction, they get involved in a risky business deal which puts their lives at stake.'
        },
        {
          id: '3',
          title: 'To All the Boys: Always and Forever',
          tahun: '2022',
          img: 'banner3.png',
          rate: '6.3',
          category: 'Drama',
          deskripsi: 'Senior year of high school takes center stage as Lara Jean returns from a family trip to Korea and considers her college plans — with and without Peter.'
        }
      ],
      movie: [
        {
          id: '1',
          title: 'Wonder Woman 1984',
          tahun: '2020',
          img: 'movie-1.png',
          rate: '7.0'
        },
        {
          id: '2',
          title: 'Below Zero',
          tahun: '2021',
          img: 'movie-2.png',
          rate: '6.4'
        },
        {
          id: '3',
          title: 'The Little Things',
          tahun: '2022',
          img: 'movie-3.png',
          rate: '6.3'
        },
        {
          id: '4',
          title: 'Outside the Wire',
          tahun: '2021',
          img: 'movie-4.png',
          rate: '6.5'
        },
        {
          id: '5',
          title: 'Black Water: Abyss',
          tahun: '2020',
          img: 'movie-5.png',
          rate: '5.1'
        },
        {
          id: '6',
          title: 'Breach',
          tahun: '2021',
          img: 'movie-6.png',
          rate: '4.6'
        },
        {
          id: '7',
          title: 'Soul',
          tahun: '2021',
          img: 'movie-7.png',
          rate: '8.3'
        },
        {
          id: '8',
          title: 'Fast & Furious Present.',
          tahun: '2021',
          img: 'movie-8.png',
          rate: '6.9'
        },
        {
          id: '9',
          title: 'The Croods: A New Age',
          tahun: '2020',
          img: 'movie-9.png',
          rate: '7.6'
        },
        {
          id: '10',
          title: 'Vanguard',
          tahun: '2020',
          img: 'movie-10.png',
          rate: '6.3'
        }
      ]
    }
  }

  replaceName (str:string) {
    str = str.replace(/\s+/g, '-').toLowerCase()
    return str
  }
}
</script>
