<template>
  <section>
    <div :class="'header '+ activeHeader">
      <b-container>
        <b-row>
          <b-col md="2" class="d-flex align-items-center justify-content-start logo">
            <nuxt-link to="/">
              <img src="@/assets/images/logo.png" alt="">
            </nuxt-link>
          </b-col>
          <b-col md="5">
            <InputTextSearch />
          </b-col>
          <b-col md="5" class="px-0">
            <ul class="menu mb-0">
              <li>
                <b-dropdown id="dropdown-left" class="dropdown-btn">
                  <template #button-content>
                    <div class="icon-category mr-1">
                      <img src="@/assets/images/category.svg" alt="">
                    </div>
                    CATEGORIES
                  </template>
                  <b-dropdown-item href="#">
                    Action
                  </b-dropdown-item>
                  <b-dropdown-item href="#">
                    Adventure
                  </b-dropdown-item>
                  <b-dropdown-item href="#">
                    Animation
                  </b-dropdown-item>
                  <b-dropdown-item href="#">
                    Comedy
                  </b-dropdown-item>
                  <b-dropdown-item href="#">
                    Crime
                  </b-dropdown-item>
                </b-dropdown>
              </li>
              <li>
                <nuxt-link to="/movies">
                  MOVIES
                </nuxt-link>
              </li>
              <li>
                <nuxt-link to="">
                  TV SHOWS
                </nuxt-link>
              </li>
              <li>
                <nuxt-link to="">
                  LOGIN
                </nuxt-link>
              </li>
            </ul>
          </b-col>
        </b-row>
      </b-container>
    </div>
  </section>
</template>
<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
@Component
export default class Header extends Vue {
  activeHeader:string = ''
  scrollPosition = 0
  created () {
    if (process.client) {
      window.addEventListener('scroll', this.handleScroll)
    }
  }

  handleScroll () {
    if (process.client) {
      this.scrollPosition = window.scrollY
      if (this.scrollPosition <= 23) {
        this.activeHeader = ''
      } else {
        this.activeHeader = 'active'
      }
    }
  }

  destroyed () {
    if (process.client) {
      window.removeEventListener('scroll', this.handleScroll)
    }
  }
}
</script>
