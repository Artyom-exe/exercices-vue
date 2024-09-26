<script setup>
import { defineProps } from "vue";

const props = defineProps({
    type: {
        type: String,
        default: "primary"
    },
    isDisabled: {
        type: Boolean,
        default: false,
    }
});
</script>

<template>
    <button 
    class="rounded shadow p-2"
    :class="{
        'bg-blue-200 text-blue-800':
        props.type === 'primary',
        'bg-red-200 text-red-800':
        props.type === 'danger',
        'bg-green-200 text-green-800':
        props.type === 'secondary', 'cursor-not-allowed': props.isDisabled
    }" :disabled="props.isDisabled">
        <slot></slot>
    </button>
</template>