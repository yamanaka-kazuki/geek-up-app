<template>
    <div class="container">
        <h2>最近の学習</h2>
        <study-component></study-component>
        <study-component></study-component>
        <study-component></study-component>
        <study-component></study-component>
        <study-component></study-component>
        <div class="display-list-btn">
            <button-component></button-component>
        </div>
    </div>
</template>

<script>
import StudyComponent from './StudyComponent.vue';
import ButtonComponent from './ButtonComponent.vue';

export default {
    components: { StudyComponent, ButtonComponent },
};
</script>

<style scoped>
.container {
    width: 500px;
    position: absolute;
    top: 100px;
    right: 30px;
}

h2 {
    font-weight: bold;
    text-align: center;
    margin-bottom: 8px;
}

.display-list-btn {
    text-align: center;
    padding-top: 12px;
}
</style>
