<template>
    <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg"
        class="w-12 h-12 group-hover:scale-110 transition-transform duration-300">
        <circle cx="50" cy="50" r="48" class="stroke-yellow-500" stroke-width="2" fill="none"></circle>
        <path d="M50 2 V15 M50 85 V98 M2 50 H15 M85 50 H98 M16 16 L25 25 M75 75 L84 84 M16 84 L25 75 M75 25 L84 16"
            class="stroke-yellow-500/50" stroke-width="4" stroke-linecap="round"></path>
        <circle cx="50" cy="50" r="35" class="fill-neutral-900 stroke-yellow-500" stroke-width="2"></circle>
        <g transform="rotate(45 50 50)">
            <rect x="45" y="20" width="10" height="60" rx="2" class="fill-white"></rect>
            <path d="M48 25 H52 M48 75 H52" class="stroke-neutral-400" stroke-width="1"></path>
        </g>
        <g transform="rotate(-45 50 50)">
            <rect x="45" y="20" width="10" height="60" rx="2" class="fill-yellow-500"></rect>
            <path d="M48 25 H52 M48 75 H52" class="stroke-yellow-700" stroke-width="1"></path>
        </g>
        <circle cx="50" cy="50" r="6" class="fill-neutral-950 stroke-white" stroke-width="1"></circle>
    </svg>
</template>
