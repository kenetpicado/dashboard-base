<template>
    <div class="bg-white text-gray-600 rounded-lg">
        <form @submit.prevent="$emit('onSubmit')">
            <div class="grid grid-cols-2 gap-4 p-8">
                <slot></slot>
            </div>


            <div class="flex items-center justify-end px-4 py-3 bg-gray-50 text-right rounded-b-lg gap-4">
                <button class="secondary-button" type="button" @click="$emit('onCancel')">
                    Cancel
                </button>
                <button type="submit" class="primary-button">
                    {{ isNew ? 'Create' : 'Update' }}
                </button>
            </div>
        </form>
    </div>
</template>

<script setup>

defineProps({
    title: {
        type: String,
        default: 'Form'
    },
    isNew: {
        type: Boolean,
        default: true
    }
})

</script>