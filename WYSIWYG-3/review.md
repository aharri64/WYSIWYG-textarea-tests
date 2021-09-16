# jQuery WYSIWYG Rich Text Editor Plugin - Froala Editor

**This one is really powerful but also pretty complicated.**

[source](https://www.jqueryscript.net/text/jQuery-WYSIWYG-Rich-Text-Editor-Plugin-Froala-Editor.html)
[demo](https://www.jqueryscript.net/demo/jQuery-WYSIWYG-Rich-Text-Editor-Plugin-Froala-Editor/)

Froala Editor is a simple clean jQuery & HTML5 based WYSIWYG rich text editor that supports auto-save, inline mode, spell check, ajax requests, image callback and many more.

The editor can be used for free only for personal and non-profit projects under the CC NC-ND license.

Please note that the download link is the latest version of the Froala Editor (version 3, removed jQuery dependency).

```js
<script>
    $(function()
    {$("#edit").editable({
        autosave: false, // Enable autosave option. Enabling autosave helps preventing data loss.
        autosaveInterval: 1000, // Time in milliseconds to define when the autosave should be triggered.
        saveURL: null, // Defines where to post the data when save is triggered. The editor will initialize a POST request to the specified URL passing the editor content in the body parameter of the HTTP request.
        blockTags: [
            "n",
            "p",
            "blockquote",
            "pre",
            "h1",
            "h2",
            "h3",
            "h4",
            "h5",
            "h6",
        ], // Defines what tags list to format a paragraph and their order.
        borderColor: "#252528", // Customize the appearance of the editor by changing the border color.
        buttons: [
            "bold",
            "italic",
            "underline",
            "strikeThrough",
            "fontSize",
            "color",
            "sep",
            "formatBlock",
            "align",
            "insertOrderedList",
            "insertUnorderedList",
            "outdent",
            "indent",
            "sep",
            "selectAll",
            "createLink",
            "insertImage",
            "undo",
            "redo",
            "html",
        ], // Defines the list of buttons that are available in the editor.
        crossDomain: false, // Make AJAX requests using CORS.
        direction: "ltr", // Sets the direction of the text.
        editorClass: "", // Set a custom class for the editor element.
        height: "auto", // Set a custom height for the editor element.
        imageMargin: 20, // Define a custom margin for image. It will be visible on the margin of the image when float left or right is active.
        imageErrorCallback: false,
        imageUploadParam: "file", // Customize the name of the param that has the image file in the upload request.
        imageUploadURL: "http://uploads.im/api", // A custom URL where to save the uploaded image.
        inlineMode: true, // Enable or disable inline mode.
        placeholder: "Type something", // Set a custom placeholder to be used when the editor body is empty.
        shortcuts: true, // Enable shortcuts. The shortcuts are visible when you hover a button in the editor.
        spellcheck: false, // Enables spellcheck.
        typingTimer: 250, // Time in milliseconds to define how long the typing pause may be without the change to be saved in the undo stack.
        width: "auto", // Set a custom width for the editor element.
    })}
    );
</script>
```
