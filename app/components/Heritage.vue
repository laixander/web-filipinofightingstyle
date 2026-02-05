<template>
    <section id="heritage" class="py-24 bg-neutral-950 relative overflow-hidden">
        <div class="absolute inset-0 bg-[url('https://www.transparenttextures.com/patterns/wood-pattern.png')] opacity-20 mix-blend-overlay pointer-events-none">
        </div>
        <div class="container mx-auto px-4 md:px-8 relative z-10">
            <div class="grid lg:grid-cols-12 gap-12 items-center">
                <div class="lg:col-span-5 relative group">
                    <div class="absolute -inset-4 border-2 border-yellow-500/30 rounded-sm translate-x-2 translate-y-2 transition-transform group-hover:translate-x-1 group-hover:translate-y-1 duration-500"></div>
                    <div class="relative overflow-hidden rounded-sm sepia-[.3] contrast-125 hover:sepia-0 transition-all duration-700">
                        <img src="https://images.unsplash.com/photo-1661153803116-12622590e75f?crop=entropy&amp;cs=tinysrgb&amp;fit=max&amp;fm=jpg&amp;q=80&amp;w=1080" alt="Filipino History" class="w-full h-auto object-cover">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <p class="text-yellow-500 font-serif italic text-sm">
                                Lapu-Lapu, the first Filipino hero
                            </p>
                        </div>
                    </div>
                </div>
                <div class="lg:col-span-7 text-neutral-300">
                    <motion.div
                        :initial="{ opacity: 0, y: 30 }"
                        :whileInView="{ opacity: 1, y: 0 }"
                        :viewport="{ once: true }"
                        :transition="{ duration: 0.8 }"
                    >
                        <h4 class="text-white font-bold uppercase tracking-[0.2em] mb-4 text-sm flex items-center gap-2">
                            <span class="w-8 h-[1px] bg-white"></span> Heritage &amp; History
                        </h4>
                        <h2 class="text-4xl md:text-5xl font-black mb-8 leading-tight font-display text-white drop-shadow-md">
                            Rooted in <br><span class="italic font-serif font-normal text-yellow-500">Resistance</span>
                        </h2>
                        <div class="space-y-6 text-lg font-light leading-relaxed text-neutral-400">
                            <p>
                                Long before the Philippines was named, its warriors defended the islands with blades and
                                hard wood. Arnis, also known as Kali or Eskrima, was born not in a dojo, but on the
                                battlefield.
                            </p>
                            <p>
                                From the Battle of Mactan where Lapu-Lapu defeated Magellan, to the clandestine training
                                during the Spanish occupation disguised as folk dance, this art form is a symbol of
                                Filipino resilience.
                            </p>
                            <p class="font-medium text-white pl-4 border-l-2 border-yellow-500">
                                In 2009, Arnis was declared the <span class="text-yellow-500">National Martial Art and Sport of the Philippines</span>, solidifying its place as a pillar of cultural identity.
                            </p>
                        </div>
                        <div class="mt-10">
                            <button class="px-8 py-3 border border-yellow-500 text-yellow-500 hover:bg-yellow-500 hover:text-black transition-all uppercase tracking-widest text-sm font-bold">
                                Read Our History
                            </button>
                        </div>
                    </motion.div>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup lang="ts">
import { motion } from "motion-v"
</script>