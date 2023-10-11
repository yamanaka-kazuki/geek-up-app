<template>
    <div class="container">
        <div class="tile is-ancestor">
            <div class="tile is-parent">
                <field-component
                    :title="runningDaysTitle"
                    :subtitle="runningDays"
                ></field-component>
            </div>
            <div class="tile is-parent">
                <field-component
                    :title="learningTimeTitle"
                    :subtitle="learningTime"
                ></field-component>
            </div>
        </div>
        <div class="tile is-ancestor">
            <div class="tile is-parent">
                <field-component
                    :title="diffTargetTimeTitle"
                    :subtitle="diffTargetTime"
                ></field-component>
            </div>
            <div class="tile is-parent">
                <field-component
                    :title="totalLearningTimeTitle"
                    :subtitle="totalLearningTime"
                ></field-component>
            </div>
        </div>
    </div>
</template>

<script>
import FieldComponent from './FieldComponent.vue';

export default {
    components: { FieldComponent },
    data() {
        return {
            runningDaysTitle: '連続学習日数',
            runningDays: '20d',
            learningTimeTitle: '今日の学習時間',
            learningTime: '3h',
            diffTargetTimeTitle: '週目標時間との差',
            diffTargetTime: '3.4h/7h',
            totalLearningTimeTitle: '総学習時間',
            totalLearningTime: '1210h30m',
        };
    },
};
</script>

<style scoped>
.container {
    position: absolute;
    top: 100px;
    left: 300px;
}
</style>
