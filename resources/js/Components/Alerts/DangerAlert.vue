<script setup>

</script>

<template>
    <div role="alert">
        <div class="bg-red-500 text-white font-bold rounded-t px-4 py-2">
            <slot name="heading" id="heading" />
        </div>
        <div class="border border-t-0 border-red-400 rounded-b bg-red-100 px-4 py-3 text-red-700">
            <p ><slot name="message" /></p>
        </div>
    </div>
</template>