<script>

export default {
    name: "JumboTron",
    data() {
        return {

        }
    },
    methods: {

    }
}
</script>

<template>
    <main>
        <div id="tag">
            <span>CURRENT SERIES</span>
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    background-image: url(../assets/jumbotron.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    height: 300px;
    padding-left: 10%;

    #tag {
        background-color: rgb(25, 98, 192);
        width: 150px;
        text-align: center;
        padding: 10px;
        position: relative;
        top: 283px;
        color: white;
    }
}
</style>