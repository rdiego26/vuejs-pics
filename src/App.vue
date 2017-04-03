<template>
  <div>
    <h1>{{ title }}</h1>
    <ul>
      <li v-for="photo in photos">
        <img :src="photo.userImageURL" :alt="photo.tags">
      </li>
    </ul>
  </div>
</template>

<script>
export default {

  data () {
    return {
      title: 'Pics',
      photos: []
    }
  },
  created () {
  	this.$http.get('https://pixabay.com/api/?lang=en&image_type=photo&key=4992052-d7a700904e127de75064f88c5&q=beach&per_page=10')
      .then(res => res.json())
      .then(photos => this.photos = photos.hits, err => console.log(err));
  }
}
</script>

<style>

</style>
