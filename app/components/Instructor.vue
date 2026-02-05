<template>
    <section id="instructor" class="py-24 bg-neutral-900">
        <div class="container mx-auto px-4 md:px-8">
            <div class="max-w-5xl mx-auto bg-neutral-950 rounded-sm overflow-hidden shadow-2xl flex flex-col md:flex-row">
                <motion.div 
                    :initial="{ opacity: 0, x: -50 }"
                    :whileInView="{ opacity: 1, x: 0 }"
                    :viewport="{ once: true }"
                    :transition="{ duration: 0.8 }"
                    class="md:w-2/5 relative"
                >
                    <img src="https://images.unsplash.com/photo-1550759807-50dc0b381a1e?crop=entropy&amp;cs=tinysrgb&amp;fit=max&amp;fm=jpg&amp;q=80&amp;w=800" alt="Head Instructor" class="w-full h-full object-cover min-h-[400px]">
                    <div class="absolute inset-0 bg-yellow-500/10 mix-blend-multiply"></div>
                </motion.div>
                <motion.div 
                    :initial="{ opacity: 0, x: 50 }"
                    :whileInView="{ opacity: 1, x: 0 }"
                    :viewport="{ once: true }"
                    :transition="{ duration: 0.8 }"
                    class="md:w-3/5 p-8 md:p-12 flex flex-col justify-center relative"
                >
                    <UIcon name="i-mingcute-quote-right-fill" class="absolute top-8 right-8 text-neutral-900 size-24 z-5" />
                    <h4 class="text-white font-bold uppercase tracking-widest text-sm mb-2">
                        Head Instructor
                    </h4>
                    <h2 class="text-3xl font-black text-white uppercase mb-1">
                        Guro Marco Reyes
                    </h2>
                    <p class="text-neutral-500 mb-6 text-sm uppercase tracking-wide">
                        6th Dan Black Belt • 25 Years Experience
                    </p>
                    <p class="text-neutral-300 italic mb-8 text-lg leading-relaxed font-serif">
                        "Arnis is not just about fighting. It is about the preservation of life, the discipline of the mind, and the connection to our ancestors. When we train, we honor them."
                    </p>
                    <div class="space-y-2 mb-8">
                        <div class="flex items-center gap-3 text-neutral-400 text-sm">
                            <span class="w-2 h-2 bg-yellow-500 rounded-full"></span>
                            <span>Direct Lineage from Grandmaster Ciriaco Cañete</span>
                        </div>
                        <div class="flex items-center gap-3 text-neutral-400 text-sm">
                            <span class="w-2 h-2 bg-yellow-500 rounded-full"></span>
                            <span>Certified FMA Instructor (Philippines Sports Commission)</span>
                        </div>
                        <div class="flex items-center gap-3 text-neutral-400 text-sm">
                            <span class="w-2 h-2 bg-yellow-500 rounded-full"></span>
                            <span>Former National Team Champion</span>
                        </div>
                    </div>
                    <button class="self-start text-white hover:text-yellow-500 font-bold uppercase tracking-widest text-sm transition-colors flex items-center gap-2">
                        Meet the Team &rarr;
                    </button>
                </motion.div>
            </div>
        </div>
    </section>
</template>
<script setup lang="ts">
import { motion } from "motion-v"
</script>