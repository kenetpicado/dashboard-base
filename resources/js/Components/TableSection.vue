<template>
    <div class="bg-white overflow-hidden border rounded-xl">
        <div class="overflow-y-auto rounded-lg m-0">
            <table class="w-full border-collapse bg-white text-left text-sm text-gray-600">
                <thead class="bg-gray-50">
                    <tr>
                        <slot name="header" />
                    </tr>
                </thead>
                <tbody class="divide-y divide-gray-100 border-t border-gray-100">
                    <slot name="body" />
                </tbody>
            </table>
        </div>
        <slot name="paginator" />
    </div>
</template>

<script setup>

</script>