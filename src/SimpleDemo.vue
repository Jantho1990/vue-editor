<template>
    <div>
        <h1>Simple Content Editor</h1>
        <editor-menu
            @requestContentUpdate="handleRequestContentUpdate"
        >

        </editor-menu>
        <editor-div ref="editorDiv"></editor-div>       
    </div>
</template>

<script>
import EditorDiv from './components/EditorDiv'
import EditorMenu from './components/EditorMenu'

export default {
    components: {
        EditorDiv,
        EditorMenu
    },
    created () {

    },
    methods: {
        handleRequestContentUpdate (type) {
            this.$refs.editorDiv.updateContent(type)
        }
    }
}
</script>

<style>

</style>
