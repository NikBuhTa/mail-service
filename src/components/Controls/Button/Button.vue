<script setup>
    import { computed } from 'vue';
    import css from './Button.module.css'

const props = defineProps(['classType']);

</script>

<template>
    <div :class="css.nav__btn_container">
        <button :class="[css.nav__btn]"><slot></slot></button>
    </div>
</template>