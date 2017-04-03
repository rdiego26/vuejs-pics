<template>
  <div>
    <h1>{{ title }}</h1>
    <ul>
      <li v-for="photo in photos">
        <img :src="photo.url" :alt="photo.title">
      </li>
    </ul>
  </div>
</template>

<script>
export default {

  data () {
    return {
      title: 'Pics',
      photos: [
        {
          url: 'http://fresh-tattoos.com/wp-content/uploads/images/baby-girls-arm-tattoo-design-3.jpg',
          title: 'Baby Girl'
        },
        {
            url: 'https://www.bigtattooplanet.com/sites/default/files/imagecache/4colwidthfull/5/attached/shiro.jpg',
            title: 'Shiro'
        },
        {
            url: 'https://s-media-cache-ak0.pinimg.com/originals/0d/72/a2/0d72a2514350ec7cd984502e7a815e5e.jpg',
            title: 'Blondie'
        }
      ]
    }
  }
}
</script>

<style>

</style>
