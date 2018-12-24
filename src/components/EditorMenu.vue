<template>
    <div class="editor-menu">
        <button @click="dispatchEvent('bold')">𝐁</button>
        <button @click="dispatchEvent('italic')">𝑖</button>
        <button @click="dispatchEvent('underline')"><span style="text-decoration: underline;">U</span></button>
        <select v-model="selectFont" @change="dispatchEvent('font-size')">
            <option value="12">12px</option>
            <option value="14">14px</option>
            <option value="16">16px</option>
            <option value="18">18px</option>
            <option value="20">20px</option>
            <option value="24">24px</option>
        </select>
    </div>
</template>

<script>
export default {
    name: 'EditorMenu',
    data () {
        return {
            selectFont: 16
        }
    },
    methods: {
        dispatchEvent (type) {
            this.$emit('requestContentUpdate', {
                type,
                data: {
                    fontSize: this.selectFont
                }
            })
        }
    }
}
</script>

<style>

</style>
