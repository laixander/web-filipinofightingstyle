<template>
    <section class="py-24 bg-neutral-950">
        <div class="container mx-auto px-4 md:px-8 max-w-4xl">
            <h2 class="text-3xl md:text-4xl font-black text-white text-center uppercase font-display mb-16">
                Frequently Asked <span class="text-yellow-500">Questions</span>
            </h2>

            <div class="space-y-4">
                <div
                    v-for="(faq, index) in faqs"
                    :key="faq.question"
                    class="border border-neutral-800 rounded-sm bg-neutral-900/50 overflow-hidden"
                >
                    <button
                        class="w-full flex justify-between items-center p-6 text-left hover:bg-neutral-800/50 transition-colors"
                        @click="toggle(index)"
                    >
                        <span class="font-bold text-white uppercase tracking-wide text-sm md:text-base pr-4">
                            {{ faq.question }}
                        </span>

                        <span
                            class="text-yellow-500 transition-transform duration-300"
                            :class="{ 'rotate-180': openIndex === index }"
                        >
                            <UIcon
                                :name="openIndex === index ? 'lucide-minus' : 'lucide-plus'"
                                class="flex size-5"
                            />
                        </span>
                    </button>
                   <AnimatePresence>
                        <motion.div
                            v-if="openIndex === index"
                            layout
                            :initial="{ height: 0, opacity: 0 }"
                            :animate="{ height: 'auto', opacity: 1 }"
                            :exit="{ height: 0, opacity: 0 }"
                            :transition="{ duration: 0.3 }"
                            class="overflow-hidden px-6 text-neutral-400 leading-relaxed border-t border-neutral-800/50"
                        >
                            <div class="py-6">
                                {{ faq.answer }}
                            </div>
                        </motion.div>
                   </AnimatePresence>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup lang="ts">
import { ref } from 'vue'
import { AnimatePresence, motion } from 'motion-v'

const openIndex = ref<number | null>(null)

const toggle = (index: number) => {
    openIndex.value = openIndex.value === index ? null : index
}

const faqs = [
  {
    question: "Do I need prior martial arts experience?",
    answer: "No. Arnis is designed to be learned from the ground up. Whether you are a complete beginner or an experienced martial artist, our curriculum adapts to your skill level."
  },
  {
    question: "Is Arnis safe for beginners?",
    answer: "Yes. Safety is our top priority. We use padded sticks for beginners and controlled drills. Sparring is optional and only introduced once you have mastered the fundamentals."
  },
  {
    question: "What equipment do I need?",
    answer: "For your first class, just wear comfortable athletic clothing. We provide the training sticks. Once you enroll, you will need to purchase your own pair of rattan sticks and a uniform."
  },
  {
    question: "Is Arnis suitable for women and children?",
    answer: "Absolutely. Arnis relies on technique, speed, and leverage rather than brute strength, making it an excellent self-defense system for women and children."
  },
  {
    question: "How do I enroll?",
    answer: "You can start by booking a free trial class using the form below or visiting our gym during operating hours. We offer flexible membership plans."
  }
];
</script>