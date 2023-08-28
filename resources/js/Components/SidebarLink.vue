<script setup>
import { computed } from 'vue';
import { Link } from '@inertiajs/vue3';  

const props = defineProps({
    href: String,
    active: Boolean,                
});

const classes = computed(() => {
    return props.active
        ? 'relative px-4 py-3 flex items-center space-x-4 rounded-xl text-white bg-gradient-to-r from-sky-600 to-cyan-400 transition duration-150 ease-in-out'
        : 'px-4 py-3 flex items-center space-x-4 rounded-md  group text-white transition duration-150 ease-in-out';
});
</script>

<template>
    <Link :href="href" :class="classes">
        <!-- <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                            <path class=" text-gray-300 group-hover:text-cyan-300" fill-rule="evenodd" d="M2 6a2 2 0 012-2h4l2 2h4a2 2 0 012 2v1H8a3 3 0 00-3 3v1.5a1.5 1.5 0 01-3 0V6z" clip-rule="evenodd" />
                            <path class=" text-gray-600 group-hover:text-cyan-600" d="M6 12a2 2 0 012-2h8a2 2 0 012 2v2a2 2 0 01-2 2H2h2a2 2 0 002-2v-2z" />
                        </svg> -->
        
          <span class="group-hover:text-cyan-400 text-white inline-flex space-x-2"> <slot /></span>               
        
    </Link>
</template>

