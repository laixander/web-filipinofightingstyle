<template>
    <section id="about" class="py-24 bg-neutral-900 relative overflow-hidden">
        <div class="absolute top-0 right-0 w-1/2 h-full bg-[url('https://www.transparenttextures.com/patterns/black-scales.png')] opacity-50 pointer-events-none mix-blend-overlay">
        </div>
        <div class="container mx-auto px-4 md:px-8">
            <div class="grid md:grid-cols-2 gap-16 items-center">
                <motion.div
                    :initial="{ opacity: 0, x: -50 }"
                    :whileInView="{ opacity: 1, x: 0 }"
                    :viewport="{ once: true }"
                    :transition="{ duration: 0.8 }"
                    class="relative"
                >
                    <div class="relative z-10 rounded-sm overflow-hidden border-4 border-neutral-800 shadow-2xl">
                        <img src="https://images.unsplash.com/photo-1637552324091-39b10b698497?crop=entropy&amp;cs=tinysrgb&amp;fit=max&amp;fm=jpg&amp;q=80&amp;w=1080" alt="Arnis Rattan Sticks" class="w-full h-[600px] object-cover hover:scale-105 transition-transform duration-700">
                        <div class="absolute inset-0 bg-gradient-to-t from-neutral-900 via-transparent to-transparent opacity-80">
                        </div>
                        <div class="absolute bottom-6 left-6 text-white max-w-xs">
                            <p class="font-serif italic text-white mb-2">
                                "The stick is an extension of the hand."
                            </p>
                        </div>
                    </div>
                    <div class="absolute -bottom-6 -right-6 w-full h-full border-2 border-yellow-500/30 z-5 rounded-sm">
                    </div>
                </motion.div>
                <motion.div
                    :initial="{ opacity: 0, x: 50 }"
                    :whileInView="{ opacity: 1, x: 0 }"
                    :viewport="{ once: true }"
                    :transition="{ duration: 0.8 }"
                >
                    <h4 class="text-white font-bold uppercase tracking-widest mb-2">
                        What is Arnis?
                    </h4>
                    <h2 class="text-4xl md:text-5xl font-black text-white mb-6 leading-tight uppercase font-display">
                        The Art of <span class="text-yellow-500">Stick &amp; Blade</span>
                    </h2>
                    <p class="text-neutral-400 text-lg mb-8 leading-relaxed">
                        Also known as <span class="text-white font-medium">Kali</span> or <span class="text-white font-medium">Eskrima</span>, Arnis is the comprehensive martial art system of the Philippines. Unlike other arts that start with empty hands, Arnis begins with weapons training—developing reaction time, precision, and a deep understanding of angles of attack.
                    </p>
                    <div class="grid sm:grid-cols-2 gap-8">
                        <template v-for="highlight in highlights" :key="highlight.title">
                            <div class="flex flex-col gap-3 group">
                                <div class="w-12 h-12 bg-neutral-800 rounded-sm flex items-center justify-center text-white group-hover:bg-yellow-500 group-hover:text-black transition-colors duration-300">
                                    <UIcon :name="highlight.icon" class="size-6"/>
                                </div>
                                <h3 class="text-white text-lg font-bold uppercase tracking-wide">
                                    {{ highlight.title }} 
                                </h3>
                                <p class="text-sm text-neutral-500 leading-relaxed">
                                    {{ highlight.description }}
                                </p>
                            </div>
                        </template>
                    </div>
                </motion.div>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import { motion } from "motion-v"
const highlights = [
    {
        icon: 'i-lucide-swords',
        title: 'Weapon-First Training',
        description: 'Start with sticks to build coordination, then translate to empty hands.'
    },
    {
        icon: 'i-lucide-shield',
        title: 'Practical Self-Defense',
        description: 'Real-world techniques focused on efficiency and neutralizing threats.'
    },
    {
        icon: 'i-lucide-wind',
        title: 'Flow-Based Movement',
        description: 'Develop fluid reflexes and adaptability through continuous motion drills.'
    },
    {
        icon: 'i-lucide-users',
        title: 'Suitable for All Ages',
        description: 'Adaptable intensity allows anyone to learn regardless of fitness level.'
    }
]  
</script>