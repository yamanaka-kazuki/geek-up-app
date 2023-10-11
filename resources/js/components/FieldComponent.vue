<template>
    <article class="tile is-child box">
        <div class="box icon-box"></div>
        <div class="content">
            <p class="title">{{ title }}</p>
            <p class="subtitle">{{ subtitle }}</p>
        </div>
    </article>
</template>

<script>
export default {
    props: {
        title: String,
        subtitle: String,
    },
};
</script>

<style scoped>
.tile {
    width: 240px;
    position: relative;
}

.icon-box {
    width: 50px;
    height: 50px;
    position: absolute;
    top: -15px;
}

.title {
    text-align: right;
    font-weight: normal;
    font-size: 16px;
    padding: 5px 0;
}

.subtitle {
    text-align: right;
    font-size: 36px;
    padding: 5px 0;
}
</style>
