# Simple Extensible WYSIWYG Editor For Web - summernote

[source](https://www.jqueryscript.net/text/wysiwyg-editor-summernote.html)
[demo](https://www.jqueryscript.net/demo/wysiwyg-editor-summernote/)

Summernote is a simple yet customizable, extensible, interactive WYSIWYG rich text editor for the web.

## Features:

- i18n support.
- Custom editor buttons.
- Works with Bootstrap framework.
- Compatible with 3rd frameworks & languages: Angular, PHP, etc.
- Switches between editor and code view modes.
- Autocomplete in the editor.
- Plugin system.
- Easy to use.
- Cross browser.

## 3rd Modules:

[Summernote Gallery Module (Demo)](https://github.com/eissasoubhi/summernote-gallery)

## Basic Usage:

1. To use the editor, include the following JavaScript and CSS files on the page.

```js
<!-- jQuery is required -->
<script src="/path/to/cdn/jquery.min.js"></script>

<!-- For <a href="https://www.jqueryscript.net/tags.php?/bootstrap 4/">Bootstrap 4</a> -->
<link rel="stylesheet" href="/path/to/dist/summernote-bs4.css" />
<script src="/path/to/dist/summernote-bs4.js"></script>

<!-- For Bootstrap 3 -->
<link rel="stylesheet" href="/path/to/dist/summernote.css" />
<script src="/path/to/dist/summernote.js"></script>

<!-- Without any framework -->
<link rel="stylesheet" href="/path/to/dist/summernote-lite.css" />
<script src="/path/to/dist/summernote-lite.js"></script>
```

2. Include a language file of your chocie on the page. All supported languages:

- summernote-ar-AR.js
- summernote-bg-BG.js
- summernote-ca-ES.js
- summernote-cs-CZ.js
- summernote-da-DK.js
- summernote-de-DE.js
- summernote-el-GR.js
- summernote-es-ES.js
- summernote-es-EU.js
- summernote-fa-IR.js
- summernote-fi-FI.js
- summernote-fr-FR.js
- summernote-gl-ES.js
- summernote-he-IL.js
- summernote-hr-HR.js
- summernote-hu-HU.js
- summernote-id-ID.js
- summernote-it-IT.js
- summernote-ja-JP.js
- summernote-ko-KR.js
- summernote-lt-LT.js
- summernote-lt-LV.js
- summernote-mn-MN.js
- summernote-nb-NO.js
- summernote-nl-NL.js
- summernote-pl-PL.js
- summernote-pt-BR.js
- summernote-pt-PT.js
- summernote-ro-RO.js
- summernote-ru-RU.js
- summernote-sk-SK.js
- summernote-sl-SI.js
- summernote-sr-RS-Latin.js
- summernote-sr-RS.js
- summernote-sv-SE.js
- summernote-ta-IN.js
- summernote-th-TH.js
- summernote-tr-TR.js
- summernote-uk-UA.js
- summernote-uz-UZ.js
- summernote-vi-VN.js
- summernote-zh-CN.js
- summernote-zh-TW.js

```js
<script src="/path/to/dist/lang/summernote-es-ES.js"></script>
```

3. Create a textarea or any other container element to hold the summernote editor.

```js
<div class="summernote">
  <p>jQueryScript.Net</p>
</div>
```

4. Attach the function to the placeholder element and done.
   $('.summernote').summernote({
   // options here
   });

5. Create an inline editor attached to the text selection using the Air mode.

```js
$(".summernote").summernote({
  airMode: true,
});
```

6. Apply an autocomplete functionality to the editor using the hint option.

```js
$(".summernote").summernote({
  hint: {
    mentions: ["jayden", "sam", "alvin", "david"],
    match: /\B@(\w*)$/,
    search: function (keyword, callback) {
      callback(
        $.grep(this.mentions, function (item) {
          return item.indexOf(keyword) == 0;
        })
      );
    },
    content: function (item) {
      return "@" + item;
    },
  },
});
```

7. This is a full list of editor buttons displayed in the toolbar. Feel free to add/remove buttons as per your needs.

- picture
- link
- video
- table
- hr
- fontname
- fontsize
- fontsizeunit
- color
- forecolor
- backcolor
- bold
- italic
- underline
- strikethrough
- superscript
- subscript
- clear
- style
- ol
- ul
- paragraph
- height
- fullscreen
- codeview
- undo
- redo
- help

```js
$(".summernote").summernote({
  toolbar: [
    ["style", ["style"]],
    ["font", ["bold", "underline", "clear"]],
    ["fontname", ["fontname"]],
    ["color", ["color"]],
    ["para", ["ul", "ol", "paragraph"]],
    ["table", ["table"]],
    ["insert", ["link", "picture", "video"]],
    ["view", ["fullscreen", "codeview", "help"]],
  ],
});
```

8. Full plugin options & callback functions to customize the summernote editor.

```js
editing: true,
modules: {
  'editor': Editor_Editor,
  'clipboard': Clipboard_Clipboard,
  'dropzone': Dropzone_Dropzone,
  'codeview': Codeview_CodeView,
  'statusbar': Statusbar_Statusbar,
  'fullscreen': Fullscreen_Fullscreen,
  'handle': Handle_Handle,
  'hintPopover': HintPopover_HintPopover,
  'autoLink': AutoLink_AutoLink,
  'autoSync': AutoSync_AutoSync,
  'autoReplace': AutoReplace_AutoReplace,
  'placeholder': Placeholder_Placeholder,
  'buttons': Buttons_Buttons,
  'toolbar': Toolbar_Toolbar,
  'linkDialog': LinkDialog_LinkDialog,
  'linkPopover': LinkPopover_LinkPopover,
  'imageDialog': ImageDialog_ImageDialog,
  'imagePopover': ImagePopover_ImagePopover,
  'tablePopover': TablePopover_TablePopover,
  'videoDialog': VideoDialog_VideoDialog,
  'helpDialog': HelpDialog_HelpDialog,
  'airPopover': AirPopover_AirPopover
},
buttons: {},
lang: 'en-US',
followingToolbar: false,
toolbarPosition: 'top',
otherStaticBar: '',
// toolbar
toolbar: [['style', ['style']], ['font', ['bold', 'underline', 'clear']], ['fontname', ['fontname']], ['color', ['color']], ['para', ['ul', 'ol', 'paragraph']], ['table', ['table']], ['insert', ['link', 'picture', 'video']], ['view', ['fullscreen', 'codeview', 'help']]],
// popover
popatmouse: true,
popover: {
  image: [['resize', ['resizeFull', 'resizeHalf', 'resizeQuarter', 'resizeNone']], ['float', ['floatLeft', 'floatRight', 'floatNone']], ['remove', ['removeMedia']]],
  link: [['link', ['linkDialogShow', 'unlink']]],
  table: [['add', ['addRowDown', 'addRowUp', 'addColLeft', 'addColRight']], ['delete', ['deleteRow', 'deleteCol', 'deleteTable']]],
  air: [['color', ['color']], ['font', ['bold', 'underline', 'clear']], ['para', ['ul', 'paragraph']], ['table', ['table']], ['insert', ['link', 'picture']], ['view', ['fullscreen', 'codeview']]]
},
// air mode: inline editor
airMode: false,
width: null,
height: null,
linkTargetBlank: true,
useProtocol: true,
defaultProtocol: 'http://',
focus: false,
tabDisabled: false,
tabSize: 4,
styleWithSpan: true,
shortcuts: true,
textareaAutoSync: true,
tooltip: 'auto',
container: null,
maxTextLength: 0,
blockquoteBreakingLevel: 2, // 0 - No break, the new paragraph remains inside the quote; 1 - Break the first blockquote in the ancestors list; 2 - Break all blockquotes, so that the new paragraph is not quoted. (default)
spellCheck: true,
disableGrammar: false,
placeholder: null,
inheritPlaceholder: false,
hintMode: 'word',
hintSelect: 'after',
hintDirection: 'bottom',
styleTags: ['p', 'blockquote', 'pre', 'h1', 'h2', 'h3', 'h4', 'h5', 'h6'],
fontNames: ['Arial', 'Arial Black', 'Comic Sans MS', 'Courier New', 'Helvetica Neue', 'Helvetica', 'Impact', 'Lucida Grande', 'Tahoma', 'Times New Roman', 'Verdana'],
fontNamesIgnoreCheck: [],
addDefaultFonts: true,
fontSizes: ['8', '9', '10', '11', '12', '14', '18', '24', '36'],
fontSizeUnits: ['px', 'pt'],
// pallete colors(n x n)
colors: [['#000000', '#424242', '#636363', '#9C9C94', '#CEC6CE', '#EFEFEF', '#F7F7F7', '#FFFFFF'], ['#FF0000', '#FF9C00', '#FFFF00', '#00FF00', '#00FFFF', '#0000FF', '#9C00FF', '#FF00FF'], ['#F7C6CE', '#FFE7CE', '#FFEFC6', '#D6EFD6', '#CEDEE7', '#CEE7F7', '#D6D6E7', '#E7D6DE'], ['#E79C9C', '#FFC69C', '#FFE79C', '#B5D6A5', '#A5C6CE', '#9CC6EF', '#B5A5D6', '#D6A5BD'], ['#E76363', '#F7AD6B', '#FFD663', '#94BD7B', '#73A5AD', '#6BADDE', '#8C7BC6', '#C67BA5'], ['#CE0000', '#E79439', '#EFC631', '#6BA54A', '#4A7B8C', '#3984C6', '#634AA5', '#A54A7B'], ['#9C0000', '#B56308', '#BD9400', '#397B21', '#104A5A', '#085294', '#311873', '#731842'], ['#630000', '#7B3900', '#846300', '#295218', '#083139', '#003163', '#21104A', '#4A1031']],
// http://chir.ag/projects/name-that-color/
colorsName: [['Black', 'Tundora', 'Dove Gray', 'Star Dust', 'Pale Slate', '<a href="https://www.jqueryscript.net/gallery/">Gallery</a>', 'Alabaster', 'White'], ['Red', 'Orange Peel', 'Yellow', 'Green', 'Cyan', 'Blue', 'Electric Violet', 'Magenta'], ['Azalea', 'Karry', 'Egg White', 'Zanah', 'Botticelli', 'Tropical Blue', 'Mischka', 'Twilight'], ['Tonys Pink', 'Peach Orange', 'Cream Brulee', 'Sprout', 'Casper', 'Perano', 'Cold Purple', 'Careys Pink'], ['Mandy', 'Rajah', 'Dandelion', 'Olivine', 'Gulf Stream', 'Viking', 'Blue Marguerite', 'Puce'], ['Guardsman Red', 'Fire Bush', 'Golden Dream', 'Chelsea Cucumber', 'Smalt Blue', 'Boston Blue', 'Butterfly Bush', 'Cadillac'], ['Sangria', 'Mai Tai', 'Buddha Gold', 'Forest Green', 'Eden', 'Venice Blue', 'Meteorite', 'Claret'], ['Rosewood', 'Cinnamon', 'Olive', 'Parsley', 'Tiber', 'Midnight Blue', 'Valentino', 'Loulou']],
colorButton: {
  foreColor: '#000000',
  backColor: '#FFFF00'
},
lineHeights: ['1.0', '1.2', '1.4', '1.5', '1.6', '1.8', '2.0', '3.0'],
tableClassName: 'table table-bordered',
insertTableMaxSize: {
  col: 10,
  row: 10
},
dialogsInBody: false, // By default, dialogs are attached in container.
dialogsFade: false,
maximumImageFileSize: null,
codemirror: {
  mode: 'text/html',
  htmlMode: true,
  lineNumbers: true
},
codeviewFilter: false,
codeviewFilterRegex: /<\/*(?:applet|b(?:ase|gsound|link)|embed|frame(?:set)?|ilayer|l(?:ayer|ink)|meta|object|s(?:cript|tyle)|t(?:itle|extarea)|xml)[^>]*?>/gi,
codeviewIframeFilter: true,
codeviewIframeWhitelistSrc: [],
codeviewIframeWhitelistSrcBase: ['www.youtube.com', 'www.youtube-nocookie.com', 'www.facebook.com', 'vine.co', 'instagram.com', 'player.vimeo.com', 'www.dailymotion.com', 'player.youku.com', 'v.qq.com'],
keyMap: {
  pc: {
    'ENTER': 'insertParagraph',
    'CTRL+Z': 'undo',
    'CTRL+Y': 'redo',
    'TAB': 'tab',
    'SHIFT+TAB': 'untab',
    'CTRL+B': 'bold',
    'CTRL+I': 'italic',
    'CTRL+U': 'underline',
    'CTRL+SHIFT+S': 'strikethrough',
    'CTRL+BACKSLASH': 'removeFormat',
    'CTRL+SHIFT+L': 'justifyLeft',
    'CTRL+SHIFT+E': 'justifyCenter',
    'CTRL+SHIFT+R': 'justifyRight',
    'CTRL+SHIFT+J': 'justifyFull',
    'CTRL+SHIFT+NUM7': 'insertUnorderedList',
    'CTRL+SHIFT+NUM8': 'insertOrderedList',
    'CTRL+LEFTBRACKET': 'outdent',
    'CTRL+RIGHTBRACKET': 'indent',
    'CTRL+NUM0': 'formatPara',
    'CTRL+NUM1': 'formatH1',
    'CTRL+NUM2': 'formatH2',
    'CTRL+NUM3': 'formatH3',
    'CTRL+NUM4': 'formatH4',
    'CTRL+NUM5': 'formatH5',
    'CTRL+NUM6': 'formatH6',
    'CTRL+ENTER': 'insertHorizontalRule',
    'CTRL+K': 'linkDialog.show'
  },
  mac: {
    'ENTER': 'insertParagraph',
    'CMD+Z': 'undo',
    'CMD+SHIFT+Z': 'redo',
    'TAB': 'tab',
    'SHIFT+TAB': 'untab',
    'CMD+B': 'bold',
    'CMD+I': 'italic',
    'CMD+U': 'underline',
    'CMD+SHIFT+S': 'strikethrough',
    'CMD+BACKSLASH': 'removeFormat',
    'CMD+SHIFT+L': 'justifyLeft',
    'CMD+SHIFT+E': 'justifyCenter',
    'CMD+SHIFT+R': 'justifyRight',
    'CMD+SHIFT+J': 'justifyFull',
    'CMD+SHIFT+NUM7': 'insertUnorderedList',
    'CMD+SHIFT+NUM8': 'insertOrderedList',
    'CMD+LEFTBRACKET': 'outdent',
    'CMD+RIGHTBRACKET': 'indent',
    'CMD+NUM0': 'formatPara',
    'CMD+NUM1': 'formatH1',
    'CMD+NUM2': 'formatH2',
    'CMD+NUM3': 'formatH3',
    'CMD+NUM4': 'formatH4',
    'CMD+NUM5': 'formatH5',
    'CMD+NUM6': 'formatH6',
    'CMD+ENTER': 'insertHorizontalRule',
    'CMD+K': 'linkDialog.show'
  }
},
icons: {
  'align': 'note-icon-align',
  'alignCenter': 'note-icon-align-center',
  'alignJustify': 'note-icon-align-justify',
  'alignLeft': 'note-icon-align-left',
  'alignRight': 'note-icon-align-right',
  'rowBelow': 'note-icon-row-below',
  'colBefore': 'note-icon-col-before',
  'colAfter': 'note-icon-col-after',
  'rowAbove': 'note-icon-row-above',
  'rowRemove': 'note-icon-row-remove',
  'colRemove': 'note-icon-col-remove',
  'indent': 'note-icon-align-indent',
  'outdent': 'note-icon-align-outdent',
  'arrowsAlt': 'note-icon-arrows-alt',
  'bold': 'note-icon-bold',
  'caret': 'note-icon-caret',
  'circle': 'note-icon-circle',
  'close': 'note-icon-close',
  'code': 'note-icon-code',
  'eraser': 'note-icon-eraser',
  'floatLeft': 'note-icon-float-left',
  'floatRight': 'note-icon-float-right',
  'font': 'note-icon-font',
  'frame': 'note-icon-frame',
  'italic': 'note-icon-italic',
  'link': 'note-icon-link',
  'unlink': 'note-icon-chain-broken',
  'magic': 'note-icon-magic',
  'menuCheck': 'note-icon-menu-check',
  'minus': 'note-icon-minus',
  'orderedlist': 'note-icon-orderedlist',
  'pencil': 'note-icon-pencil',
  'picture': 'note-icon-picture',
  'question': 'note-icon-question',
  'redo': 'note-icon-redo',
  'rollback': 'note-icon-rollback',
  'square': 'note-icon-square',
  'strikethrough': 'note-icon-strikethrough',
  'subscript': 'note-icon-subscript',
  'superscript': 'note-icon-superscript',
  'table': 'note-icon-table',
  'textHeight': 'note-icon-text-height',
  'trash': 'note-icon-trash',
  'underline': 'note-icon-underline',
  'undo': 'note-icon-undo',
  'unorderedlist': 'note-icon-unorderedlist',
  'video': 'note-icon-video'
}
```

9. Callback functions available:

```js
$('.summernote').summernote({
  callbacks: {
    onBeforeCommand: null,
    onBlur: null,
    onBlurCodeview: null,
    onChange: : function(contents, $editable) {
      console.log('onChange:', contents, $editable);
    }
    onChangeCodeview: null,
    onDialogShown: null,
    onEnter: null,
    onFocus: null,
    onImageLinkInsert: null,
    onImageUpload: function(files) {
      // upload image to server and create imgNode...
      $summernote.summernote('insertNode', imgNode);
    }
    onImageUploadError: null,
    onInit: null,
    onKeydown: null,
    onKeyup: null,
    onMousedown: null,
    onMouseup: null,
    onPaste: null,
    on<a href="https://www.jqueryscript.net/tags.php?/Scroll/">Scroll</a>: null
  },
});
```

10. Create your own editor buttons as follows:

```js
var newButton = function (context) {
  var ui = $.summernote.ui;

  // create button
  var button = ui.button({
    contents: "New",
    tooltip: "A New Button",
    click: function () {
      // invoke insertText method with 'new' on editor module.
      context.invoke("editor.insertText", "new");
    },
  });

  return button.render(); // return button as jquery object
};

$(".summernote").summernote({
  toolbar: [["mybutton", ["new"]]],

  buttons: {
    new: newButton,
  },
});
```
