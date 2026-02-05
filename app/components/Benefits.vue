<template>
    <section id="benefits" class="py-24 bg-neutral-950 relative">
        <div class="container mx-auto px-4 md:px-8 relative z-10">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-black text-white mb-4 uppercase font-display tracking-wide">
                    Why Train <span class="text-yellow-500">Arnis?</span>
                </h2>
                <div class="w-24 h-1 bg-white mx-auto"></div>
            </div>
            <div class="grid md:grid-cols-3 gap-8 max-w-6xl mx-auto">
                <motion.div
                    v-for="(benefit, idx) in benefits" 
                    :key="idx"
                    :initial="{ opacity: 0, y: 30 }"
                    :whileInView="{ opacity: 1, y: 0 }"
                    :viewport="{ once: true }"
                    :transition="{ delay: idx * 0.1, duration: 0.5 }"
                    :whileHover="{ y: -10 }"
                    class="bg-neutral-900 border border-neutral-800 p-8 rounded-sm hover:border-yellow-500/50 transition-colors group relative overflow-hidden"
                >
                    <div class="absolute top-0 right-0 p-4 opacity-5 group-hover:opacity-10 transition-opacity">
                        <UIcon :name="benefit.icon" class="size-25" />
                    </div>
                    <div class="w-14 h-14 bg-neutral-950 border border-neutral-700 rounded-sm flex items-center justify-center text-white mb-6 group-hover:bg-yellow-500 group-hover:text-black group-hover:border-yellow-500 transition-all duration-300">
                        <UIcon :name="benefit.icon" class="size-7" />
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3 uppercase tracking-wide group-hover:text-yellow-500 transition-colors">
                        {{ benefit.title }}
                    </h3>
                    <p class="text-neutral-400 text-sm leading-relaxed">
                        {{ benefit.description }}
                    </p>
                </motion.div>
            </div>
        </div>
    </section>
</template>
<script setup lang="ts">
import { motion } from "motion-v"
const benefits = [
    {
        icon: 'i-lucide-shield-check',
        title: 'Self-Defense Readiness',
        description: 'Master techniques that work in real-life situations, focusing on leverage and awareness.'
    },
    {
        icon: 'i-lucide-brain-circuit',
        title: 'Mental Discipline',
        description: 'Sharpen your focus, decision-making speed, and tactical thinking under pressure.'
    },
    {   
        icon: 'i-lucide-activity',
        title: 'Physical Fitness',
        description: 'Improve your strength, endurance, and agility through targeted training.'
    },
    {
        icon: 'i-lucide-landmark',
        title: 'Cultural Heritage',
        description: 'Connect with Filipino history and preserve an art form passed down through generations.'
    },
    {
        icon: 'i-lucide-users',
        title: 'Community & Respect',
        description: 'Join a brotherhood of practitioners united by mutual respect and shared growth.'
    }
]
</script>