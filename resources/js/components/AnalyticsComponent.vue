<template>
    <div class="container">
        <div class="tile is-ancestor">
            <div class="tile is-parent">
                <field-component
                    :title="runningDays.title"
                    :subtitle="runningDays.data"
                    :icon-name="runningDays.icon"
                    :bgcolor="runningDays.bgcolor"
                ></field-component>
            </div>
            <div class="tile is-parent">
                <field-component
                    :title="learningTime.title"
                    :subtitle="learningTime.data"
                    :icon-name="learningTime.icon"
                    :bgcolor="learningTime.bgcolor"
                ></field-component>
            </div>
        </div>
        <div class="tile is-ancestor">
            <div class="tile is-parent">
                <field-component
                    :title="diffTargetTime.title"
                    :subtitle="diffTargetTime.data"
                    :icon-name="diffTargetTime.icon"
                    :bgcolor="diffTargetTime.bgcolor"
                ></field-component>
            </div>
            <div class="tile is-parent">
                <field-component
                    :title="totalLearningTime.title"
                    :subtitle="totalLearningTime.data"
                    :icon-name="totalLearningTime.icon"
                    :bgcolor="totalLearningTime.bgcolor"
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
            runningDays: {
                title: '連続学習日数',
                data: '20d',
                icon: 'fire',
                bgcolor: '#ff7f50',
            },
            learningTime: {
                title: '今日の学習時間',
                data: '3h',
                icon: 'timelapse',
                bgcolor: '#00ff00',
            },
            diffTargetTime: {
                title: '週目標時間との差',
                data: '3.4h/7h',
                icon: 'flag-variant',
                bgcolor: '#8a2be2',
            },
            totalLearningTime: {
                title: '総学習時間',
                data: '1210h30m',
                icon: 'chart-timeline-variant',
                bgcolor: '#4169e1',
            },
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
