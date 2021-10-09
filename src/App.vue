<template>
    <div id="app">
        <CKEditor
            v-model="editor"
            v-bind:config="config"
            editor-url="/ckeditor-4.16.2/ckeditor.js"
        />
    </div>
</template>

<script>
import CKEditor from 'ckeditor4-vue/dist/legacy';

export default {
    name: 'App',
    components: {
        CKEditor: CKEditor.component,
    },

    data () {
        return {
            editor: "initial content",
        };
    },

    computed: {
        config () {
            return {
                removePlugins: 'exportpdf',
                skin: 'moono-lisa',
            };
        },
    },
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
