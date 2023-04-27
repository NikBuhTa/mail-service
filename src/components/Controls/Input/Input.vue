<script setup>
    import css from './Input.module.css'
</script>

<template>
    <div :class="css.nav__container">
        <input :class="css.nav__input" type="text" placeholder="Поиск сообщения"/>
        <img :class="css.search" src="../../../assets/search.svg"/>
    </div>
</template>

<style lang="scss" scoped>

</style>