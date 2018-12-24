<template>
    <div class="editor-menu">
        <button @click="dispatchEvent('bold')">𝐁</button>
        <button @click="dispatchEvent('italic')">𝑖</button>
        <button @click="dispatchEvent('underline')"><span style="text-decoration: underline;">U</span></button>
    </div>
</template>

<script>
export default {
    name: 'EditorMenu',
    methods: {
        dispatchEvent (type) {
            this.$emit('requestContentUpdate', type)
        }
    }
}
</script>

<style>

</style>
