<script setup>
    import { computed } from 'vue';
    import css from './Letter.module.css'
    import Checkbox from '../../Controls/Checkbox/Checkbox.vue';

    const props = defineProps(['isImportant', 'date', 'isChecked', 'text']);

</script>

<template>
    <div :class="css.letter">
        <Checkbox />
        <div :class="css.letter__sender"><slot name="sender"></slot></div>
        <div :class="css.letter__title"><slot name="title"></slot></div>
        <div :class="css.letter_date">{{ `${props.date.getHours()}:${props.date.getMinutes()}` }}</div>
    </div>
</template>