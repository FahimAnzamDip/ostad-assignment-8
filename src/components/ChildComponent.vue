<template>
    <div class="bg-gray-200 p-4 rounded-md">
        <h1 class="text-1xl font-bold text-gray-700">Child Component</h1>
        <p>{{ message }}</p>
        <button @click="messageEmitted" class="border-0 bg-indigo-500 text-white font-medium rounded shadow px-3 py-2 mt-4">
            Click me to get a message in parent component
        </button>
    </div>
</template>

<script setup>
import { inject, defineEmits } from 'vue'

const message = inject('message')

const emit = defineEmits(['messageEmitted'])

const messageEmitted = () => {
    emit('messageEmitted', 'This is a message from child component')
}
</script>
