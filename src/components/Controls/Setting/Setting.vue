<script setup>
    import css from './Setting.module.css'
</script>

<template>
    <div :class="css.setting__container">
        <span :class="css.setting__link"><slot></slot></span>
    </div>
</template>