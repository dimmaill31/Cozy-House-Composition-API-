<template>
    <div class="modal">
        <slot></slot>
    </div>
</template>

<script setup>
    const props = defineProps({
        modalShowStatus: {
            type: Boolean,
            required: true,
        }
    })
</script>

<style scoped>

.modal{
    position: fixed;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    background-color: rgba(0, 0, 0, 0.6);
    justify-content: center;
    align-items: center;
    display: flex;
    visibility: visible;
}

</style>