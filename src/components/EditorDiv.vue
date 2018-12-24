<template>
    <div class="editor-container">
        <div ref="editor" class="editor" contenteditable="true">

        </div>
    </div>
</template>

<script>
export default {
    name: 'EditorDiv',
    created () {
        document.execCommand('styleWithCSS', false, true)
    },
    methods: {
        updateContent (updateType, data) {
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
                case 'font-size':
                debugger
                    const text = window.getSelection().toString()
                    const span = `<span class="font f${data.fontSize}px">${text}</span>`
                    document.execCommand('insertHTML', false, span)
                    // document.execCommand('formatBlock', false, 'div')
                    // const node = window.getSelection().focusNode.parentNode
                    // node.classList.add('test')

                    break
                default:
                    console.log(`Error: type '${updateType}' not found.`)
            }
        }
    }
}
</script>

<style lang="scss">
@import '../assets/styles/font-size';

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
