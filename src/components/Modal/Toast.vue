<script setup>
import { Teleport, Transition  } from 'vue';
import css from './Modal.module.css';

defineEmits(['close']);
defineProps(['isShown']);

</script>

<template>
    <Teleport to='#toast'>
        <Transition>
            <div v-if="isShown" :class="css.modal">
                <button @click="$emit('close')" :class="css.modal__button">&times;</button>
                <p :class="css.modal__adtext">Здесь могла быть ваша реклама @Vue.js</p>
            </div>
        </Transition>
    </Teleport>
</template>

<style scoped>
    .v-enter-active,
    .v-leave-active {
        transition: opacity 300ms ease;
    }

    .v-enter-from {
        opacity: 0;
    }

    .v-leave-to {
        opacity: 0;
        transform: translateZ(100px);
    }
</style>