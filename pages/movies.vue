<template>
  <section>
    <section class="bg-dark-gray pb-5">
      <div class="bg-gray box-backdrop" />
      <div class="box-content pt-4">
        <b-container>
          <b-row class="mb-5">
            <b-col md="12">
              <div class="title-section">
                <div class="pita" />
                <h4>MOVIES</h4>
              </div>
            </b-col>
          </b-row>
          <section>
            <b-row>
              <b-col md="3">
                <div class="box-filter">
                  <div class="column-filter title-filter">
                    Sort Result By
                  </div>
                  <div class="column-filter">
                    <b-dropdown class="dropdown-filter">
                      <template #button-content>
                        {{ selectedSort }}
                      </template>
                      <template v-for="(sort, i) in listSort">
                        <b-dropdown-item :key="i" href="#" @click="select(sort.label)">
                          {{ sort.label }}
                        </b-dropdown-item>
                      </template>
                    </b-dropdown>
                  </div>
                  <div class="column-filter title-filter">
                    Genres
                  </div>
                  <div class="column-filter border-bottom-0">
                    <ul class="pl-0 list-genre">
                      <li v-for="(item, i) in listGenre" :key="i">
                        <label class="container-check d-flex align-items-center mb-0 pl-0 pr-2">
                          <input
                            v-model="genre"
                            type="checkbox"
                            name="genre"
                            :value="item.value"
                          >
                          <span class="checkmark" />
                          <span class="caption-check">{{ item.label }}</span>
                        </label>
                      </li>
                    </ul>
                  </div>
                </div>
              </b-col>
              <b-col md="9">
                <div class="row d-flex justify-content-center">
                  <div v-for="(item, i) in movie" :key="i" class="col-md-3 px-3 mb-4">
                    <ProductMovie :img="item.img" :title="item.title" :tahun="item.tahun" :rate="item.rate" :url="replaceName(item.title)" />
                  </div>
                  <button class="btn-link btn-more">
                    Load More
                  </button>
                </div>
              </b-col>
            </b-row>
          </section>
        </b-container>
      </div>
    </section>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
@Component
export default class Movies extends Vue {
  selectedSort:string | null = 'Popularity'
  genre = []
  movie = [
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
    },
    {
      id: '11',
      title: 'Tenet',
      tahun: '2020',
      img: 'movie-11.png',
      rate: '7.3'
    },
    {
      id: '12',
      title: '100% Wolf',
      tahun: '2020',
      img: 'movie-12.png',
      rate: '5.9'
    }
  ]

  listGenre = [
    {
      id: '1',
      value: 'GEN01',
      label: 'Action'
    },
    {
      id: '2',
      value: 'GEN02',
      label: 'Adventure'
    },
    {
      id: '3',
      value: 'GEN03',
      label: 'Animation'
    },
    {
      id: '4',
      value: 'GEN04',
      label: 'Comedy'
    },
    {
      id: '5',
      value: 'GEN05',
      label: 'Crime'
    },
    {
      id: '6',
      value: 'GEN06',
      label: 'Documentary'
    },
    {
      id: '7',
      value: 'GEN07',
      label: 'Drama'
    },
    {
      id: '8',
      value: 'GEN08',
      label: 'Family'
    },
    {
      id: '9',
      value: 'GEN09',
      label: 'Fantasy'
    },
    {
      id: '10',
      value: 'GEN10',
      label: 'History'
    },
    {
      id: '11',
      value: 'GEN11',
      label: 'Horror'
    }
  ]

  listSort = [
    {
      value: 'popularity_asc',
      label: 'Popularity Ascending '
    },
    {
      value: 'popularity_desc',
      label: 'Popularity Descending '
    },
    {
      value: 'realese_asc',
      label: 'Realese Date Ascending '
    },
    {
      value: 'realese_desc',
      label: 'Realese Date Descending '
    },
    {
      value: 'rating_asc',
      label: 'Rating Ascending '
    },
    {
      value: 'rating_desc',
      label: 'Rating Descending '
    }
  ]

  select (label:string) {
    this.selectedSort = label
  }

  replaceName (str:string) {
    str = str.replace(/\s+/g, '-').toLowerCase()
    return str
  }
}
</script>
