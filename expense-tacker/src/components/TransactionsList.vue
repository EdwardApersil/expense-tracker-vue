<template>
    <h3>History</h3>
    <ul class="list" id="list">
        <li class="plus" v-for="t in trans" :key="t.id" :class="[t.money < 0 ? 'minus' : 'plus']">
            {{ t.name }} <span>+${{ t.money }}</span>
            <button class="delete-btn">x</button>
        </li>
    </ul>
</template>

<script setup>
    import { defineProps } from 'vue';

    const props = defineProps({
        trans: {
            typeof: Array,
            required: true,
        }
    })
</script>