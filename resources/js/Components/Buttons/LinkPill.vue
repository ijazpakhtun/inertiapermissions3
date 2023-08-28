
<script setup >
import { Link } from '@inertiajs/vue3';

defineProps({
    href: {
        type: String,
        required: true,
    },
});
</script>


<template >

    <div class="px-2 py-5 ">
                   <Link :href="href"  class="bg-indigo-600 hover:bg-indigo-800  text-white font-bold py-3 px-4 rounded border border-indigo-700  "><slot /></Link>

    </div>
</template>