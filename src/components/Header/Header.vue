<script setup>

    import css from './Header.module.css';
    import Input from '../Controls/Input/Input.vue'
    import Logo from '../Logo/Logo.vue'
    import Button from '../Controls/Button/Button.vue'
</script>

<template>
    <header :class="css.header">
        <Logo>F&amp;P mail</Logo>
        <nav :class="css.nav">
            <Input />
            <Button ><img :class="css.nav__image" src="../../assets/help.svg"/></Button>
        </nav>
    </header>
</template>

<style scoped>

</style>