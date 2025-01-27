<template>
  <b-input-group class="mt-3 input-group-search">
    <template #prepend>
      <b-input-group-text class="img-prepend">
        <img src="@/assets/images/movie_icon.svg" alt="">
      </b-input-group-text>
    </template>
    <b-form-input class="text-search" placeholder="Find Movie" />
    <template #append>
      <b-input-group-text class="img-append">
        <img src="@/assets/images/search-icon.svg" alt="">
      </b-input-group-text>
    </template>
  </b-input-group>
</template>
<script>
export default {
}
</script>
