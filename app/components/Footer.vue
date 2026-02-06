<template>
    <footer class="bg-neutral-950 pt-20 pb-10 border-t border-neutral-900">
        <div class="container mx-auto px-4 md:px-8">
            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-12 mb-16">
                <div>
                    <a href="#" class="flex items-center gap-3 group mb-6">
                        <Logo :size="40" />
                        <div class="flex flex-col">
                            <span class="text-lg font-black tracking-wider text-white uppercase font-display leading-none">
                                Filipino
                            </span>
                            <span class="text-xs font-bold tracking-[0.2em] text-yellow-500 uppercase font-display leading-none">
                                Fighting Style
                            </span>
                        </div>
                    </a>
                    <p class="text-neutral-500 text-sm leading-relaxed mb-6">
                        Preserving the art of Filipino stick fighting through disciplined training and cultural education.
                    </p>
                    <div class="flex gap-4">
                        <a href="#" class="text-neutral-400 hover:text-white transition-colors">
                            <UIcon name="i-lucide-facebook" class="size-5" />
                        </a>
                        <a href="#" class="text-neutral-400 hover:text-white transition-colors">
                            <UIcon name="i-lucide-instagram" class="size-5" />
                        </a>
                        <a href="#" class="text-neutral-400 hover:text-white transition-colors">
                            <UIcon name="i-lucide-youtube" class="size-5" />
                        </a>
                    </div>
                </div>
                <div>
                    <h4 class="text-white font-bold uppercase tracking-widest mb-6 text-sm">Quick Links</h4>
                    <ul class="space-y-3 text-sm text-neutral-400">
                        <li><a href="#about" class="hover:text-yellow-500 transition-colors">About Arnis</a></li>
                        <li><a href="#programs" class="hover:text-yellow-500 transition-colors">Training Programs</a>
                        </li>
                        <li><a href="#instructor" class="hover:text-yellow-500 transition-colors">Instructors</a></li>
                        <li><a href="#schedule" class="hover:text-yellow-500 transition-colors">Class Schedule</a></li>
                        <li><a href="#heritage" class="hover:text-yellow-500 transition-colors">History</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-white font-bold uppercase tracking-widest mb-6 text-sm">Contact Us</h4>
                    <ul class="space-y-4 text-sm text-neutral-400">
                        <li class="flex items-start gap-3">
                            <UIcon name="i-lucide-map-pin" class="size-5 text-yellow-500 shrink-0 mt-1" />
                            <span>123 Warrior's Way,<br>Makati City, Philippines</span>
                        </li>
                        <li class="flex items-center gap-3">
                            <UIcon name="i-lucide-phone" class="size-5 text-yellow-500 shrink-0" />
                            <span>+63 917 123 4567</span>
                        </li>
                        <li class="flex items-center gap-3">
                            <UIcon name="i-lucide-mail" class="size-5 text-yellow-500 shrink-0" />
                            <span>train@arnis-academy.com</span>
                        </li>
                    </ul>
                </div>
                <div class="bg-neutral-900 rounded-sm h-48 md:h-auto overflow-hidden relative group">
                    <img src="https://plus.unsplash.com/premium_photo-1712828731398-ad18ac5a9748?crop=entropy&amp;cs=tinysrgb&amp;fit=max&amp;fm=jpg&amp;q=80&amp;w=400" alt="Map Location" class="w-full h-full object-cover opacity-50 group-hover:opacity-70 transition-opacity">
                    <div class="absolute inset-0 flex items-center justify-center">
                        <button class="bg-white/10 backdrop-blur-md border border-white/20 text-white px-4 py-2 text-xs font-bold uppercase hover:bg-white hover:text-black transition-all">
                            View on Map
                        </button>
                    </div>
                </div>
            </div>
            <div class="border-t border-neutral-900 pt-8 flex flex-col md:flex-row justify-between items-center gap-4 text-xs text-neutral-600 uppercase tracking-wide">
                <p>&copy; 2026 Filipino Fighting Style. All rights reserved.</p>
                <div class="flex gap-6">
                    <a href="#" class="hover:text-neutral-400">Privacy Policy</a>
                    <a href="#" class="hover:text-neutral-400">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>
</template>