<script>
    import Editor from '@tinymce/tinymce-svelte';
    let conf = {
        toolbar: 'undo redo | styles | bold italic | alignleft aligncenter alignright alignjustify | ' +
            'bullist numlist outdent indent | link image | preview media | ' +
            'forecolor backcolor emoticons | help',
        menubar: false,
        plugins: [
            'advlist', 'autolink', 'link', 'image', 'lists', 'charmap', 'preview', 'anchor', 'pagebreak',
            'searchreplace', 'wordcount', 'visualblocks', 'visualchars', 'code', 'fullscreen', 'insertdatetime',
            'media', 'table', 'emoticons', 'template', 'help'
        ],

    }
    let value = 'some content';
    let text = '';
</script>

<main>
    <h1>Hello Tiny</h1>
    <Editor {conf} apiKey="" bind:value={value} bind:text={text} />
    <div>1- {text}</div>
    <div>2- {@html value}</div>

    3-<textarea bind:value={value}></textarea>

</main>
