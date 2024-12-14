<script setup lang="ts">defineProps<{
    isChecked?:boolean | false
}>()
</script>

<template>
    <label for=: class="{ 'checked': isChecked }">
        <input type="checkbox":checked="isChecked" >
        <slot></slot>
    </label>

</template>

<style scoped>
    label{
        cursor: pointer;
    }
    .checked{
        text-decoration:line-through;
    }
</style>
