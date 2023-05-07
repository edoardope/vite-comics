<script>

export default {
    name: "CardComic",
    props: ["comicDetails"],
    data() {
        return {

        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div>
        <img :src="comicDetails.thumb" alt="">
        <span>{{ comicDetails.series }}</span>
        <br>
        <span>{{ comicDetails.type }}</span>
        <br>
        <span>{{ comicDetails.price }}</span>
    </div>
</template>

<style lang="scss" scoped>
span {
    color: white;
}

div {
    color: white;
    flex-basis: calc(90% / 4);
    text-align: center;
    margin-bottom: 50px;

    img {
        width: 100%;
        height: 80%
    }
}
</style>