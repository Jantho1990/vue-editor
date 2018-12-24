<template>
    <div class="editor-container">
        <div ref="editor" class="editor" contenteditable="true">

        </div>
    </div>
</template>

<script>
export default {
    name: 'EditorDiv',
    methods: {
        updateContent (updateType) {
            switch (updateType) {
                case 'bold':
                    document.execCommand('bold', false, null)
                    break
                case 'italic':
                    document.execCommand('italic', false, null)
                    break
                case 'underline':
                    document.execCommand('underline', false, null)
                    break
                default:
                    console.log(`Error: type '${updateType}' not found.`)
            }
        }
    }
}
</script>

<style>
.editor-container {
    border: 1px solid hsl(0, 50%, 50%);
    height: 200px;
    width: 50vw;
    margin: auto;
    text-align: left;
}

.editor {
    height: 100%;
    width: 100%;
    min-height: 100%;
    background: hsl(90, 20%, 90%);
}
</style>
