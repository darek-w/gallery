<template>
    <div class="gallery">
        <v-container fluid>
            <v-row justify="space-around">
                <v-col  
                    class="d-flex child-flex mb-6 pt-0 pb-0 custom-border"
                    cols="12"
                    sm="6"
                    md="4" 
                    v-for="galleryItem in items" 
                    :key="galleryItem.imageUrl"
                >
                    <GalleryItem :url="galleryItem.imageUrl" />
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>

import GalleryItem from '@/components/Gallery/GalleryItem'

export default {
    components: {
        GalleryItem
    },
    props: {
        items: {
            required: true,
            type: Array
        }
    },
}
</script>

<style lang="scss" scoped>
@import '~vuetify/src/styles/settings/_variables';
$gray: #ccc;
$customBorder: 2px $gray solid;

@media #{map-get($display-breakpoints, 'md-and-up')} {
    .custom-border {
        &:nth-child(3n - 1),
        &:nth-child(3n - 2) {
            border-right: $customBorder;
        }
    }
}

@media #{map-get($display-breakpoints, 'sm-only')} {
    .custom-border {
        &:nth-child(odd) {
            border-right: $customBorder;
        }
    }
}
</style>