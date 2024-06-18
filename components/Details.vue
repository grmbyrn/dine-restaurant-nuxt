<template>
    <div class="text-center pb-32">
        <div>
            <img src="@/assets/images/homepage/family-gathering-mobile.jpg" class="mx-auto mt-20 shadow-2xl" alt="logo">
        </div>
        <div>
            <ul class="mt-12">
                <li @click="showContent('family')" :class="{ 'font-semibold': selectedEvent === 'family' }"
                    class="hover:cursor-pointer leading-7 tracking-widest">Family Gathering</li>
                <li @click="showContent('special')" :class="{ 'font-semibold': selectedEvent === 'special' }"
                    class="hover:cursor-pointer leading-7 tracking-widest">Special Events</li>
                <li @click="showContent('social')" :class="{ 'font-semibold': selectedEvent === 'social' }"
                    class="hover:cursor-pointer leading-7 tracking-widest">Social Events</li>
            </ul>

            <div>
                <div v-if="selectedEvent === 'family'" class="mt-6">
                    <h2 class="text-3xl">Family Gathering</h2>
                    <p class="mt-3.5">
                        We love catering for entire families. So please bring everyone along for a special meal with
                        your
                        loved
                        ones. We’ll provide a memorable experience for all.
                    </p>
                </div>

                <div v-if="selectedEvent === 'special'" class="mt-6">
                    <h2 class="text-3xl">Special Events</h2>
                    <p>
                        Whether it’s a romantic dinner or special date you’re celebrating with others we’ll look after
                        you.
                        We’ll be
                        sure to mark your special date with an unforgettable meal.
                    </p>
                </div>

                <div v-if="selectedEvent === 'social'" class="mt-6">
                    <h2 class="text-3xl">Social Events</h2>
                    <p>
                        Are you looking to have a larger social event? No problem! We’re more than happy to cater for
                        big
                        parties.
                        We’ll work with you to make your event a hit with everyone.
                    </p>
                </div>
                <Button />
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const selectedEvent = ref('family')

const showContent = (event) => {
    selectedEvent.value = event
}
</script>