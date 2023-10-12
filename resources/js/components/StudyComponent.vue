<template>
    <div class="card">
        <div class="card-content">
            <div class="content">学習記録アプリケーション「geekup」開発</div>
            <div class="tag-container">
                <section>
                    <b-field>
                        <b-tag icon="vuejs" class="tech-tag" rounded
                            >Vue.js</b-tag
                        >
                    </b-field>
                </section>
                <section>
                    <b-field>
                        <b-tag icon="laravel" class="tech-tag" rounded
                            >Laravel</b-tag
                        >
                    </b-field>
                </section>
            </div>
        </div>
        <div class="detail-link"><a>開く</a></div>
    </div>
</template>

<script>
export default {};
</script>

<style scoped>
.card {
    width: 480px;
    height: 80px;
    display: flex;
    margin-bottom: 12px;
}

.content {
    font-weight: bold;
    font-size: 16px;
    margin-top: -8px;
}

.tag-container {
    display: flex;
    gap: 4px;
    margin-top: -15px;
}

.detail-link {
    position: absolute;
    top: 50%;
    right: 5%;
    transform: translateY(-50%);
    -webkit-transform: translateY(-50%);
    -ms-transform: translateY(-50%);
}
</style>
