<template>
    <b-navbar type="is-info">
        <template #brand>
            <b-navbar-item tag="router-link" :to="{ path: '/' }">
                <img :src="'/images/geekup-logo.png'" alt="Geekup's Logo" />
            </b-navbar-item>
        </template>
        <template #end>
            <b-navbar-item>
                <b-icon icon="menu" size="is-medium" type="is-white"> </b-icon>
            </b-navbar-item>
        </template>
    </b-navbar>
</template>

<script>
export default {};
</script>

<style></style>
