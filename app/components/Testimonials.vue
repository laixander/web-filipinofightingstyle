<template>
    <section class="py-24 bg-neutral-950 overflow-hidden">
        <div class="container mx-auto px-4 md:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-black text-white uppercase font-display mb-4">
                    Student <span class="text-yellow-500">Stories</span>
                </h2>
                <div class="w-16 h-1 bg-white mx-auto"></div>
            </div>

            <div class="mx-auto max-w-6xl">
                <UCarousel v-slot="{ item }" loop dots :autoplay="{ delay: 2000 }" :items="testimonials"
                    :ui="uiCarousel">
                    <div
                        class="bg-neutral-900 p-8 rounded-sm border border-neutral-800 h-full flex flex-col min-h-[250px]">
                        <!-- Rating -->
                        <div class="flex mb-4 gap-1">
                            <UIcon v-for="star in 5" :key="star" name="i-lucide-star" class="size-4"
                                :class="star <= item.rating ? 'text-yellow-500' : 'text-neutral-600'" />
                        </div>

                        <p class="text-neutral-300 mb-6 flex-grow leading-relaxed">
                            "{{ item.text }}"
                        </p>

                        <div>
                            <h4 class="text-white font-bold uppercase tracking-wide text-sm">
                                {{ item.name }}
                            </h4>
                            <span class="text-neutral-500 text-xs uppercase tracking-wider">
                                {{ item.role }}
                            </span>
                        </div>
                    </div>
                </UCarousel>
            </div>
        </div>
    </section>
</template>
<script setup lang="ts">
const uiCarousel = {
    item: 'px-4 basis-full lg:basis-1/3',
    dots: 'absolute inset-x-0 -bottom-7 flex flex-wrap items-center justify-center gap-5',
    dot: [
        'cursor-pointer size-1.5 bg-muted rounded-full focus:outline-none focus-visible:ring-2 focus-visible:ring-primary',
        'transition',
        'data-[state=active]:bg-yellow-500'
    ]
}
const testimonials = [
    {
        name: "Sarah Jenkins",
        role: "Student, 2 Years",
        text: "Arnis gave me a confidence I never knew I had. The community is supportive, and the training is practical from day one.",
        rating: 5
    },
    {
        name: "Mark Dizon",
        role: "Advanced Practitioner",
        text: "Connecting with my Filipino heritage through martial arts has been a life-changing journey. The instructors are world-class.",
        rating: 5
    },
    {
        name: "Elena Rodriguez",
        role: "Parent",
        text: "My son has learned so much discipline and respect. It's amazing to see him grow and learn about our culture.",
        rating: 5
    },
    {
        name: "James Chen",
        role: "Beginner",
        text: "Intense but rewarding. I love that we start with weapons immediately. It's unlike any other martial art I've tried.",
        rating: 4
    },
    {
        name: "Maria Lopez",
        role: "Student, 6 Months",
        text: "The techniques are practical and effective. I've already seen improvements in my reflexes and confidence.",
        rating: 4
    }
];
</script>