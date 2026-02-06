<template>
    <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg" :style="sizeStyle" :class="[
        'transition-transform duration-300',
        hover && 'group-hover:scale-110',
        props.class
    ]">
        <circle cx="50" cy="50" r="48" class="stroke-yellow-500" stroke-width="2" fill="none" />

        <path d="M50 2 V15 M50 85 V98 M2 50 H15 M85 50 H98
         M16 16 L25 25 M75 75 L84 84
         M16 84 L25 75 M75 25 L84 16" class="stroke-yellow-500/50" stroke-width="4" stroke-linecap="round" />

        <circle cx="50" cy="50" r="35" class="fill-neutral-900 stroke-yellow-500" stroke-width="2" />

        <g transform="rotate(45 50 50)">
            <rect x="45" y="20" width="10" height="60" rx="2" class="fill-white" />
            <path d="M48 25 H52 M48 75 H52" class="stroke-neutral-400" stroke-width="1" />
        </g>

        <g transform="rotate(-45 50 50)">
            <rect x="45" y="20" width="10" height="60" rx="2" class="fill-yellow-500" />
            <path d="M48 25 H52 M48 75 H52" class="stroke-yellow-700" stroke-width="1" />
        </g>

        <circle cx="50" cy="50" r="6" class="fill-neutral-950 stroke-white" stroke-width="1" />
    </svg>
</template>
<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps({
    /** Size in px or Tailwind size (e.g. 48, "3rem") */
    size: {
        type: [Number, String],
        default: 48
    },
    /** Enable hover scale animation */
    hover: {
        type: Boolean,
        default: true
    },
    /** Extra classes */
    class: {
        type: String,
        default: ''
    }
})

const sizeStyle = computed(() => {
    const value = typeof props.size === 'number'
        ? `${props.size}px`
        : props.size

    return {
        width: value,
        height: value
    }
})
</script>