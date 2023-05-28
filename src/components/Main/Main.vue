<script setup>
    import Setting from '../Controls/Setting/Setting.vue';
    import Letter from './Letter/Letter.vue';
    import css from './Main.module.css'
    import { Letters } from '../../utils/mock.js'
</script>

<template>
    <main :class="css.main">
        <aside :class="css.aside">
            <h2 :class="css.aside__title">Настройки</h2>
            <ul :class="css.settings">
                <li :class="css.settings__setting"><Setting>Здесь будут настройки</Setting></li>
                <li :class="css.settings__setting"><Setting>Когда-нибудь</Setting></li>
                <li :class="css.settings__setting"><Setting>Возможно даже скоро</Setting></li>
                <li :class="css.settings__setting"><Setting>А может и нет</Setting></li>
            </ul>
        </aside>
        <section :class="css.letters">
            <Letter v-for="{title, sender, date, isChecked, isImportant, text} in Letters"
                :date="date"
                :isChecked="isChecked"
                :isImportant="isImportant"
                :text="text"
            >
                <template #title>{{ title }}</template>
                <template #sender>{{ sender }}</template>
            </Letter>
        </section>
    </main>
</template>