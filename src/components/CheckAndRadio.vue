<script setup>
import { ref } from 'vue';

const isChecked = ref(false);
const selectedOption = ref('');

const options = ref([
    { key: '100', value: 'Java' },
    { key: '200', value: 'PHP' },
    { key: '300', value: 'Python' }
]);
</script>

<template>
    <div class="container">
        <div class="card">
            <h1>Form Elements</h1>

            <!-- Checkbox Section -->
            <div class="section">
                <label class="checkbox-label">
                    <input
                        type="checkbox"
                        v-model="isChecked"
                        class="checkbox-input"
                    />
                    <span class="checkbox-text">Agree to terms and conditions</span>
                </label>
                <p class="status-text">
                    Is checked: <span class="status-value">{{ isChecked ? 'Yes' : 'No' }}</span>
                </p>
            </div>

            <!-- Radio Button Section -->
            <div class="section">
                <p class="radio-title">Select your favorite language:</p>
                <div class="radio-group">
                    <span v-for="option in options" :key="option.key" class="radio-option">
                        <input
                            type="radio"
                            v-model="selectedOption"
                            :value="option.key"
                            :id="`option-${option.key}`"
                            class="radio-input"
                        />
                        <label :for="`option-${option.key}`" class="radio-text">
                            {{ option.value }}
                        </label>
                    </span>
                </div>
                <p class="status-text">
                    Selected Option: <span class="status-value">{{ selectedOption || 'None' }}</span>
                </p>
            </div>
        </div>
    </div>
</template>

<style>
/* General CSS for the component */
body {
    margin: 0;
    font-family: 'Inter', sans-serif; /* Using Inter as per instructions */
}

.container {
    min-height: 100vh;
    background-color: #f3f4f6; /* bg-gray-100 */
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 1rem; /* p-4 */
}

.card {
    background-color: #ffffff; /* bg-white */
    padding: 2rem; /* p-8 */
    border-radius: 0.5rem; /* rounded-lg */
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05); /* shadow-xl */
    max-width: 28rem; /* max-w-md */
    width: 100%; /* w-full */
    text-align: center;
}

h1 {
    font-size: 1.875rem; /* text-3xl */
    font-weight: 700; /* font-bold */
    color: #1f2937; /* text-gray-800 */
    margin-bottom: 1.5rem; /* mb-6 */
}

.section {
    margin-bottom: 1.5rem; /* mb-6 */
    text-align: left;
}

.checkbox-label,
.radio-option {
    display: inline-flex;
    align-items: center;
    cursor: pointer;
}

.checkbox-input,
.radio-input {
    height: 1.25rem; /* h-5 */
    width: 1.25rem; /* w-5 */
    color: #2563eb; /* text-blue-600 */
    border-radius: 0.25rem; /* rounded */
    border: 1px solid #d1d5db; /* default border */
    transition: all 150ms ease-in-out; /* transition duration-150 ease-in-out */
}

.checkbox-input:focus,
.radio-input:focus {
    outline: none;
    box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.5); /* focus:ring-2 focus:ring-blue-500 focus:ring-opacity-75 */
}

.checkbox-text,
.radio-text {
    margin-left: 0.5rem; /* ml-2 */
    color: #374151; /* text-gray-700 */
    font-size: 1.125rem; /* text-lg */
}

.status-text {
    margin-top: 0.5rem; /* mt-2 */
    color: #4b5563; /* text-gray-600 */
    font-size: 0.875rem; /* text-sm */
}

.status-value {
    font-weight: 600; /* font-semibold */
}

.radio-title {
    color: #374151; /* text-gray-700 */
    font-size: 1.125rem; /* text-lg */
    font-weight: 600; /* font-semibold */
    margin-bottom: 0.75rem; /* mb-3 */
}

.radio-group {
    display: flex;
    flex-direction: column;
    gap: 0.75rem; /* space-y-3 */
}
</style>
