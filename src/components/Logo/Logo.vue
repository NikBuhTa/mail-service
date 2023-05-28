<script setup>
    import css from './Logo.module.css'
</script>

<template>
    <div :class="css.logo">
        <h1 :class="css.logo__title"><slot></slot></h1>
    </div>
</template>