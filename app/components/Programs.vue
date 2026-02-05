<template>
    <section id="programs" class="py-24 bg-neutral-900 relative">
        <div class="absolute inset-0 bg-[url('https://www.transparenttextures.com/patterns/carbon-fibre.png')] opacity-20 mix-blend-overlay">
        </div>
        <div class="container mx-auto px-4 md:px-8 relative z-10">
            <div class="flex flex-col md:flex-row justify-between items-end mb-16 gap-6">
                <div>
                    <h4 class="text-white font-bold uppercase tracking-widest mb-2">
                        Curriculum
                    </h4>
                    <h2 class="text-3xl md:text-5xl font-black text-white uppercase font-display">
                        Training <span class="text-neutral-500">Programs</span>
                    </h2>
                </div>
                <button class="text-white border-b border-yellow-500 pb-1 hover:text-yellow-500 transition-colors uppercase text-sm tracking-widest">
                    View Full Schedule
                </button>
            </div>
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
                <motion.div v-for="(program, idx) in programs" 
                    :key="idx"
                    :initial="{ opacity: 0, scale: 0.95 }"
                    :whileInView="{ opacity: 1, scale: 1 }"
                    :viewport="{ once: true }"
                    :transition="{ delay: idx * 0.1 }"
                    :class="[
                        'p-8 rounded-sm border flex flex-col justify-between group cursor-pointer transition-all duration-300',
                        program.highlight 
                            ? 'bg-neutral-800 border-yellow-500 hover:bg-neutral-800/80' 
                            : 'bg-neutral-950 border-neutral-800 hover:border-neutral-600'
                    ]"
                >
                    <div>
                        <div class="flex justify-between items-start mb-6">
                            <div :class="[
                                program.highlight ? 'p-3 rounded-sm bg-yellow-500 text-black' : 'p-3 rounded-sm bg-neutral-900 text-neutral-400 group-hover:text-white'
                            ]">
                                <UIcon :name="program.icon" class="flex size-6" />
                            </div>
                            <span v-if="program.highlight" class="bg-white text-black text-xs font-bold px-2 py-1 rounded-full uppercase tracking-wider">Most
                            Highlight</span>
                        </div>
                        <h3 class="text-xl font-bold text-white uppercase tracking-wide mb-2">
                            {{ program.title }}
                        </h3>
                        <div class="flex items-center gap-4 text-xs font-medium uppercase tracking-wider mb-4 opacity-70">
                            <span :class="[
                                program.highlight ? 'text-yellow-400' : 'text-neutral-500'
                            ]">{{ program.level }}</span>
                            <span class="w-1 h-1 rounded-full bg-current"></span>
                            <span class="flex items-center gap-1">
                                <UIcon name="i-lucide-clock" class="size-4" /> {{ program.duration }}
                            </span>
                        </div>
                        <p :class="[
                            'text-sm mb-8 leading-relaxed',
                            program.highlight ? 'text-neutral-300' : 'text-neutral-400'
                        ]">
                            {{ program.description }}
                        </p>
                    </div>
                    <div 
                        class="flex items-center gap-2 text-sm font-bold uppercase tracking-widest transition-transform group-hover:translate-x-2"
                        :class="[
                            program.highlight ? 'text-yellow-500' : 'text-white'
                        ]"
                    >
                        Register
                        <UIcon name="i-lucide-arrow-right" class="size-4" />
                    </div>
                </motion.div>
            </div>
        </div>
    </section>
</template>
<script setup lang="ts">
import { motion } from "motion-v"
const programs = [
    {
        icon: 'i-lucide-star',
        title: 'Beginner Arnis',
        level: 'Level 1',
        duration: '12 Weeks',
        description: 'Foundation of stance, striking mechanics, and basic defense.',
        highlight: false
    },
    {
        icon: 'i-lucide-swords',
        title: 'Advanced Combat',
        level: 'Level 2-3',
        duration: 'Ongoing',
        description: 'Complex flow drills, sparring, and multiple opponent scenarios.',
        highlight: true
    },
    {
        icon: 'i-lucide-users',
        title: 'Kids & Youth',
        level: 'Ages 7-15',
        duration: 'Semester',
        description: 'Discipline, coordination, and confidence building in a safe environment.',
        highlight: false
    },
    {
        icon: 'i-lucide-shield',
        title: 'Adult Self-Defense',
        level: 'Open',
        duration: 'Workshop',
        description: 'Intensive crash course on street survival and awareness.',
        highlight: false
    },
    {
        icon: 'i-lucide-award',
        title: 'Instructor Path',
        level: 'Certification',
        duration: '1 Year',
        description: 'Master the curriculum and learn how to teach the next generation.',
        highlight: false
    }
]
</script>