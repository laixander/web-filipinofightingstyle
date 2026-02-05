<template>
    <section class="py-24 bg-neutral-950 text-white relative overflow-hidden">
        <div class="container mx-auto px-4 md:px-8 max-w-5xl">
            <div class="text-center mb-20">
                <h4 class="text-white font-bold uppercase tracking-widest mb-2">
                    Progression
                </h4>
                <h2 class="text-3xl md:text-5xl font-black uppercase font-display">
                    The <span class="text-yellow-500">Warrior's</span> Path
                </h2>
            </div>
            <div class="relative">
                <div class="absolute left-[19px] md:left-1/2 top-0 bottom-0 w-0.5 bg-neutral-800 -translate-x-1/2 hidden md:block">
                </div>
                <div class="absolute left-[19px] top-0 bottom-0 w-0.5 bg-neutral-800 md:hidden"></div>
                <div class="space-y-12">
                    <motion.div 
                        v-for="(step, idx) in steps" 
                        :key="idx" 
                        :initial="{ opacity: 0, y: 50 }"
                        :whileInView="{ opacity: 1, y: 0 }" 
                        :viewport="{ once: true, margin: '-100px' }"
                        :transition="{ duration: 0.6, delay: idx * 0.1 }" 
                        :class="[
                            'relative flex flex-col md:flex-row gap-8 md:gap-0 items-start md:items-center',
                            idx % 2 !== 0 ? 'md:flex-row-reverse' : ''
                        ]"
                    >
                        <!-- Number Bubble -->
                        <div class="absolute left-0 md:left-1/2 w-10 h-10 bg-neutral-900 border-2 border-yellow-500 rounded-full flex items-center justify-center z-10 -translate-x-1/2 shrink-0 md:translate-x-[-50%] translate-y-1">
                            <span class="text-yellow-500 font-bold text-xs">
                                {{ step.step }}
                            </span>
                        </div>

                        <!-- Content -->
                        <div :class="[
                            'pl-12 md:pl-0 md:w-1/2',
                            idx % 2 === 0
                                ? 'md:pr-16 md:text-right'
                                : 'md:pl-16'
                        ]">
                            <h3 class="text-xl md:text-2xl font-bold uppercase mb-2 text-white">
                                {{ step.title }}
                            </h3>
                            <p class="text-neutral-400 leading-relaxed text-sm md:text-base">
                                {{ step.description }}
                            </p>
                        </div>

                        <!-- Empty side for balance -->
                        <div class="hidden md:block md:w-1/2" />
                    </motion.div>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup lang="ts">
import { motion } from "motion-v"
const steps = [
    {
        title: "Single Stick (Solo Baston)",
        description: "The foundation. Learn the 12 strikes, blocking, and disarming techniques with a single weapon.",
        step: "01"
    },
    {
        title: "Double Stick (Doble Baston)",
        description: "Develop ambidexterity and complex weaving patterns (Sinawali) to overwhelm opponents.",
        step: "02"
    },
    {
        title: "Blade Concepts (Espada y Daga)",
        description: "Transitioning stick mechanics to edged weapons. Understanding lethal angles and immediate counters.",
        step: "03"
    },
    {
        title: "Empty Hand (Mano y Mano)",
        description: "Panantukan (dirty boxing) and Dumog (grappling) derived from weapon movements.",
        step: "04"
    },
    {
        title: "Flow Drills & Sparring",
        description: "Putting it all together in dynamic, non-choreographed exchanges to test reflexes.",
        step: "05"
    }
];
</script>