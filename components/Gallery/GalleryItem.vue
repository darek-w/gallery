<template>
    <v-img
        :src="url"
        aspect-ratio="1"
    ></v-img>
</template>

<script>
export default {
    props: {
        url: {
            required: true,
            type: String
        }
    },
}
</script>
