<template>
    <nav :class="[
        'fixed w-full z-50 transition-all duration-300 font-sans border-b',
        isScrolled
            ? 'bg-neutral-950/95 border-yellow-500/10 shadow-lg backdrop-blur-md py-4'
            : 'bg-transparent border-transparent py-6'
    ]">
        <motion.div 
            :initial="{ opacity: 0, y: -30 }"
            :animate="{ opacity: 1, y: 0 }"
            :transition="{ duration: 0.8, ease: 'easeOut' }"
            class="container mx-auto px-4 md:px-8 flex justify-between items-center"
        >
            <a href="#" class="flex items-center gap-3 group">
                <Logo />
                <div class="flex flex-col">
                    <span class="text-lg font-black tracking-wider text-white uppercase font-display leading-none">
                        Filipino
                    </span>
                    <span class="text-sm font-bold tracking-[0.2em] text-yellow-500 uppercase font-display leading-none">
                        Fighting Style
                    </span>
                </div>
            </a>
            <div class="hidden md:flex items-center gap-8">
                <a href="#about" class="text-neutral-300 hover:text-white font-medium text-sm tracking-widest uppercase transition-colors">
                    About
                </a>
                <a href="#benefits" class="text-neutral-300 hover:text-white font-medium text-sm tracking-widest uppercase transition-colors">
                    Benefits
                </a>
                <a href="#programs" class="text-neutral-300 hover:text-white font-medium text-sm tracking-widest uppercase transition-colors">
                    Programs
                </a>
                <a href="#heritage" class="text-neutral-300 hover:text-white font-medium text-sm tracking-widest uppercase transition-colors">
                    Heritage
                </a>
                <a ref="#instructor" class="text-neutral-300 hover:text-white font-medium text-sm tracking-widest uppercase transition-colors">
                    Instructor
                </a>
                <a href="#enroll" class="bg-yellow-500 hover:bg-yellow-400 text-black px-6 py-2 rounded-sm font-bold uppercase tracking-wider text-sm transition-all hover:shadow-[0_0_15px_rgba(234,179,8,0.5)]">
                    Join Now
                </a>
            </div>
            <button class="md:hidden text-white hover:text-yellow-500 transition-colors">
                <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-menu">
                    <line x1="4" x2="20" y1="12" y2="12"></line>
                    <line x1="4" x2="20" y1="6" y2="6"></line>
                    <line x1="4" x2="20" y1="18" y2="18"></line>
                </svg>
            </button>
        </motion.div>
    </nav>
</template>
<script setup lang="ts">
import { motion } from "motion-v"
import { ref, onMounted, onUnmounted } from 'vue'

const isOpen = ref(false)

const isScrolled = ref(false);
const onScroll = () => {
    isScrolled.value = window.scrollY > 50
}

onMounted(() => window.addEventListener('scroll', onScroll))
onUnmounted(() => window.removeEventListener('scroll', onScroll))
</script>