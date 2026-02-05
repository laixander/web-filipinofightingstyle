<template>
    <section class="relative h-screen min-h-[800px] flex items-center justify-center overflow-hidden bg-neutral-950">
        <div class="absolute inset-0 z-0">
            <img src="https://images.unsplash.com/photo-1564452879279-03d854bd2401?crop=entropy&amp;cs=tinysrgb&amp;fit=max&amp;fm=jpg&amp;q=80&amp;w=1920" alt="Arnis Stick Fighting" class="w-full h-full object-cover opacity-60">
            <div class="absolute inset-0 bg-gradient-to-t from-neutral-950 via-neutral-950/70 to-neutral-950/40"></div>
            <div class="absolute inset-0 bg-[url('https://www.transparenttextures.com/patterns/cubes.png')] opacity-10 mix-blend-overlay">
            </div>
        </div>
        <div class="container mx-auto px-4 relative z-10 pt-20">
            <div class="max-w-4xl mx-auto text-center">
                <motion.div
                    :initial="{ opacity: 0, y: 30 }"
                    :animate="{ opacity: 1, y: 0 }"
                    :transition="{ duration: 0.8, ease: 'easeOut' }"
                >
                    <div class="inline-flex items-center gap-2 px-3 py-1 mb-6 border border-white/30 rounded-full bg-white/5 backdrop-blur-sm">
                        <span class="w-2 h-2 rounded-full bg-yellow-500 animate-pulse"></span>
                        <span class="text-white text-xs font-bold tracking-[0.2em] uppercase">
                            The National Martial Art of the Philippines
                        </span>
                    </div>
                    <h1 class="text-5xl md:text-7xl lg:text-8xl font-black text-white mb-6 leading-tight tracking-tight uppercase font-display">
                        <span class="block text-yellow-500 drop-shadow-lg">Precision.</span>
                        <span class="block drop-shadow-lg">Speed. Tradition.</span>
                    </h1>
                    <p class="text-lg md:text-2xl text-neutral-300 mb-10 max-w-2xl mx-auto font-light leading-relaxed">
                        The official martial art of the Philippines — blending self-defense, discipline, and cultural heritage into a flowing art of war.
                    </p>
                    <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
                        <motion.button 
                            :whileHover="{ scale: 1.05 }"
                            :whileTap="{ scale: 0.95 }"
                            class="w-full sm:w-auto px-8 py-4 bg-yellow-500 text-black font-bold uppercase tracking-widest text-sm rounded-sm hover:bg-yellow-400 transition-colors shadow-[0_0_20px_rgba(234,179,8,0.4)] flex items-center justify-center gap-2"
                        >
                            Enroll Now <UIcon name="i-lucide-arrow-right" class="size-4"/>
                        </motion.button>
                        <motion.button 
                            :whileHover="{ scale: 1.05 }"
                            :whileTap="{ scale: 0.95 }" 
                            class="w-full sm:w-auto px-8 py-4 bg-transparent border border-white/20 text-white font-bold uppercase tracking-widest text-sm rounded-sm hover:bg-white/10 transition-colors flex items-center justify-center gap-2 group"
                        >
                            Learn More <UIcon name="i-lucide-chevron-right" class="size-4 group-hover:translate-x-1 transition-transform"/>
                        </motion.button>
                    </div>
                </motion.div>
            </div>
        </div>

        <motion.div 
            :initial="{ opacity: 0 }"
            :animate="{ opacity: 1 }"
            :transition="{ delay: 1, duration: 1 }" 
            className="absolute bottom-10 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 text-neutral-500"
        >
            <span class="text-xs uppercase tracking-widest">Scroll</span>
            <div class="w-[1px] h-12 bg-gradient-to-b from-yellow-500 to-transparent"></div>
        </motion.div>
    </section>
</template>
<script setup lang="ts">
import { motion } from "motion-v"
</script>