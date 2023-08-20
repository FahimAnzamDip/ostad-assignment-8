<template>
    <div class="flex justify-center items-center h-screen">
        <ParentComponent :message="'Just a random message from parent component...'"/>
    </div>
</template>

<script setup>
import ParentComponent from "./components/ParentComponent.vue";
</script>
