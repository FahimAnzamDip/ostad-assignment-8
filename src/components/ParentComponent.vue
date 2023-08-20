<template>
    <div class="bg-gray-200 p-4 rounded-md">
        <h1 class="text-2xl font-bold text-gray-700">Parent Component</h1>
        <p>{{ receivedMessage }}</p>
        <ChildComponent @messageEmitted="showMessage" />
    </div>
</template>

<script setup>
import { defineProps, provide, ref } from "vue";
import ChildComponent from "./ChildComponent.vue";

const props = defineProps({
    message: String,
});

provide("message", props.message);

const receivedMessage = ref('');

const showMessage = (message) => {
    receivedMessage.value = message;
};
</script>
