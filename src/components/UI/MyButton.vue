<template>
    <button class="btn" @click="$emit('click')">
        <slot></slot>
    </button>
</template>

<script>
export default {
    name: 'my-button'
}
</script>

<style >
.btn {
    padding: 10px 15px;
    background: none;
    color: teal;
    border: 1px solid teal;
}
</style>