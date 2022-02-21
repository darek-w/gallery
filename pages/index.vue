<template>
    <div class="gallery-page">
        <GalleryList :items="galleryItems" />
    </div>
</template>

<script>
import GalleryList from '@/components/Gallery/GalleryList'

import { ref } from '@vue/composition-api'

export default {
  name: 'IndexPage',
  components: {
    GalleryList
  },
  setup() {
    const galleryItems = ref([
      {
        imageUrl: 'https://wallpaperaccess.com/full/2465994.jpg'
      },
      {
        imageUrl: 'https://images.wallpaperscraft.com/image/single/background_black_white_wooden_surface_board_18564_300x168.jpg'
      },
      {
        imageUrl: 'https://speckyboy.com/wp-content/uploads/2020/11/minimal-desktop-wallpaper-high-resolution-4k-01.jpg'
      },
       {
        imageUrl: 'https://wallpaperaccess.com/full/2465994.jpg'
      },
      {
        imageUrl: 'https://images.wallpaperscraft.com/image/single/background_black_white_wooden_surface_board_18564_300x168.jpg'
      },
      {
        imageUrl: 'https://speckyboy.com/wp-content/uploads/2020/11/minimal-desktop-wallpaper-high-resolution-4k-01.jpg'
      }
    ])
    return {
      galleryItems
    }
  }
}
</script>
