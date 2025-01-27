<template>
  <main>
    <section v-if="$route.params.slug">
      <section>
        <div class="banner-detail-movie">
          <img src="@/assets/images/banner-detail.png" alt="">
        </div>
        <div class="line-score">
          <div class="box-content-detail">
            <b-container>
              <b-row>
                <b-col md="3">
                  <div class="movie-detail">
                    <img src="@/assets/images/movie-1.png" alt="">
                  </div>
                </b-col>
                <b-col md="9">
                  <div class="info-movie-detail">
                    <div class="tahun">
                      2020
                    </div>
                    <h1>Wonder Woman 1984</h1>
                    <div class="category">
                      Fantasy, Action, Adventure
                    </div>
                  </div>
                  <div class="box-rating">
                    <ul class="mb-0">
                      <li>
                        <div class="rate-page-detail pr-3">
                          <img src="@/assets/images/Star.svg" alt="">
                          7.0
                        </div>
                        <div class="item-detail">
                          <div class="title-item">
                            User Score
                          </div>
                          <div class="value-item">
                            3621 Votes
                          </div>
                        </div>
                      </li>
                      <li>
                        <div class="item-detail">
                          <div class="title-item">
                            Status
                          </div>
                          <div class="value-item">
                            Released
                          </div>
                        </div>
                      </li>
                      <li>
                        <div class="item-detail">
                          <div class="title-item">
                            language
                          </div>
                          <div class="value-item">
                            english
                          </div>
                        </div>
                      </li>
                      <li>
                        <div class="item-detail">
                          <div class="title-item">
                            budget
                          </div>
                          <div class="value-item">
                            $200,000,000.00
                          </div>
                        </div>
                      </li>
                      <li>
                        <div class="item-detail">
                          <div class="title-item">
                            production
                          </div>
                          <div class="value-item">
                            DC Entertainment
                          </div>
                        </div>
                      </li>
                    </ul>
                  </div>
                  <div class="overview">
                    <h5>OVERVIEW</h5>
                    <p>
                      Wonder Woman comes into conflict with the Soviet Union during the Cold<br>
                      War in the 1980s and finds a formidable foe by the name of the Cheetah.
                    </p>
                  </div>
                </b-col>
              </b-row>
            </b-container>
          </div>
        </div>
      </section>
      <section class="bg-white">
        <div class="box-review mb-5">
          <b-container>
            <b-row class="mb-3">
              <b-col cols="12">
                <div class="overview">
                  <h5>REVIEWS</h5>
                </div>
              </b-col>
            </b-row>
            <b-row>
              <b-col md="6" class="mb-3">
                <div class="box-testimoni">
                  <b-row class="mb-4">
                    <b-col md="6">
                      <div class="profile-testimoni d-flex align-items-center justify-content-start">
                        <img src="@/assets/images/no-img.png" class="mr-2" alt="">
                        <div class="body-profile-testi">
                          <div class="name">
                            SWITCH.
                          </div>
                          <div class="date">
                            December 18, 2020
                          </div>
                        </div>
                      </div>
                    </b-col>
                    <b-col md="6" class="d-flex justify-content-end">
                      <div class="rate-testi pr-3">
                        <sup><img src="@/assets/images/Star.svg" alt=""></sup>
                        7.0
                      </div>
                    </b-col>
                  </b-row>
                  <b-row>
                    <b-col md="12">
                      <div class="desc-testi elipsis-8">
                        <p>
                          It isn't as easy as saying 'Wonder Woman 1984' is a good or bad movie.
                          The pieces are there, and there are moments I adore, but it does come across as a bit
                          of a mess, even though the action sequences are breathtaking. If you're a fan of the
                          original film, you'll be more willing to take the ride, but for those more indifferent,
                          it may be a bit of a blander sit. If you can and are planning to watch it, the theatrical
                          experience is the way to go - there is nothing like seeing these stunning sets, fun action scenes and hearing Zimmer's
                          jaw-dropping score like on the big screen. - Chris dos Santos...
                          <nuxt-link to="">
                            read the rest.
                          </nuxt-link>
                        </p>
                      </div>
                    </b-col>
                  </b-row>
                </div>
              </b-col>
              <b-col md="6" class="mb-3">
                <div class="box-testimoni">
                  <b-row class="mb-4">
                    <b-col md="6">
                      <div class="profile-testimoni d-flex align-items-center justify-content-start">
                        <img src="@/assets/images/no-img.png" class="mr-2" alt="">
                        <div class="body-profile-testi">
                          <div class="name">
                            msbreviews
                          </div>
                          <div class="date">
                            December 18, 2020
                          </div>
                        </div>
                      </div>
                    </b-col>
                    <b-col md="6" class="d-flex justify-content-end">
                      <div class="rate-testi pr-3">
                        <sup><img src="@/assets/images/Star.svg" alt=""></sup>
                        8.0
                      </div>
                    </b-col>
                  </b-row>
                  <b-row>
                    <b-col md="12">
                      <div class="desc-testi elipsis-8">
                        <p>
                          If you enjoy reading my Spoiler-Free reviews, please follow my blog @ https://www.msbreviews.com
                        </p>
                        <p>
                          The superhero genre has been growing exponentially during the last decade, so it's bizarre to go through an entire year with only Birds of Prey and The New Mutants instead of literally dozens of films from both Marvel and DC. Thankfully, Warner Bros. decided to release Wonder Woman 1984 before the year's end, but not without a catch. Most people will only have the possibility of watching one of the few blockbusters of 2020 through HBO Max, a streaming service only
                        </p>
                      </div>
                    </b-col>
                  </b-row>
                </div>
              </b-col>
            </b-row>
          </b-container>
        </div>
      </section>
      <section class="bg-dark-gray pt-5 pb-3">
        <b-container>
          <b-row>
            <b-col cols="12">
              <div class="title-rekomen text-uppercase mb-4">
                <h3>RECOMMENDATION MOVIES</h3>
              </div>
            </b-col>
          </b-row>
          <div class="row d-flex justify-content-center">
            <div v-for="(item, i) in movie" :key="i" class="col-md-5ths px-3 mb-4">
              <ProductMovie :img="item.img" :title="item.title" :tahun="item.tahun" :rate="item.rate" :url="replaceName(item.title)" />
            </div>
          </div>
        </b-container>
      </section>
    </section>
  </main>
</template>
<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
@Component
export default class Slug extends Vue {
  movie = [
    {
      id: '1',
      title: 'The New Mutants',
      tahun: '2020',
      img: 'movie-13.png',
      rate: '7.0'
    },
    {
      id: '2',
      title: 'Soul',
      tahun: '2021',
      img: 'movie-14.png',
      rate: '6.4'
    },
    {
      id: '3',
      title: 'Tenet',
      tahun: '2022',
      img: 'movie-15.png',
      rate: '6.3'
    },
    {
      id: '4',
      title: 'The Old Guard',
      tahun: '2021',
      img: 'movie-16.png',
      rate: '7.0'
    },
    {
      id: '5',
      title: 'Project Power',
      tahun: '2020',
      img: 'movie-17.png',
      rate: '7.0'
    }
  ]

  replaceName (str:string) {
    str = str.replace(/\s+/g, '-').toLowerCase()
    return str
  }
}
</script>
