[source](https://www.jqueryscript.net/text/Rich-Text-Editor-jQuery-RichText.html)
[demo](https://www.jqueryscript.net/demo/Rich-Text-Editor-jQuery-RichText/)

Just another jQuery implementation of the WYSIWYG rich text editor that uses Font Awesome Iconic Font for the editor icons. Licensed under the AGPL-3.0.

How to use it:

1. Load the required Font Awesome 4:

1

<link rel="stylesheet" href="//netdna.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
2. Load the richtext.min.css to style the editor.

1

<link rel="stylesheet" href="richtext.min.css">
3. Load JQuery library and the richtext.min.js at the end of the webpage.

1

<link rel="stylesheet" href="richtext.min.css">
4. Create a normal textarea element for the editor.

1
<textarea class="content" name="example"></textarea> 5. Calling the plugin will transform the textarea element into a basic WYSIWYG rich text editor.

1
$('.content').richText(); 6. Customize the editor by overriding the following parameter options.

001
$('.content').richText({
002
// text formatting
003
bold:true,
004
italic:true,
005
underline:true,
006

007
// text alignment
008
leftAlign:true,
009
centerAlign:true,
010
rightAlign:true,
011
justify:true,
012

013
// lists
014
ol:true,
015
ul:true,
016

017
// title
018
heading:true,
019

020
// fonts
021
fonts:true,
022
fontList: ["Arial",
023
"Arial Black",
024
"Comic Sans MS",
025
"Courier New",
026
"Geneva",
027
"Georgia",
028
"Helvetica",
029
"Impact",
030
"Lucida Console",
031
"Tahoma",
032
"Times New Roman",
033
"Verdana"
034
],
035
fontColor:true,
036
fontSize:true,
037

038
// uploads
039
imageUpload:true,
040
fileUpload:true,
041

042
// media
043
<a href="https://www.jqueryscript.net/tags.php?/video/">video</a>Embed:true,
044

045
// link
046
urls:true,
047

048
// tables
049
table:true,
050

051
// code
052
removeStyles:true,
053
code:true,
054

055
// colors
056
colors: [],
057

058
// dropdowns
059
fileHTML:'',
060
imageHTML:'',
061

062
// translations
063
translations: {
064
'title':'Title',
065
'white':'White',
066
'black':'Black',
067
'brown':'Brown',
068
'beige':'Beige',
069
'darkBlue':'Dark Blue',
070
'blue':'Blue',
071
'lightBlue':'Light Blue',
072
'darkRed':'Dark Red',
073
'red':'Red',
074
'darkGreen':'Dark Green',
075
'green':'Green',
076
'purple':'Purple',
077
'darkTurquois':'Dark Turquois',
078
'turquois':'Turquois',
079
'darkOrange':'Dark Orange',
080
'orange':'Orange',
081
'yellow':'Yellow',
082
'imageURL':'Image URL',
083
'fileURL':'File URL',
084
'linkText':'Link text',
085
'url':'URL',
086
'size':'Size',
087
'responsive':'<a href="https://www.jqueryscript.net/tags.php?/Responsive/">Responsive</a>',
088
'text':'Text',
089
'openIn':'Open in',
090
'sameTab':'Same tab',
091
'newTab':'New tab',
092
'align':'Align',
093
'left':'Left',
094
'justify':'Justify',
095
'center':'Center',
096
'right':'Right',
097
'rows':'Rows',
098
'columns':'Columns',
099
'add':'Add',
100
'pleaseEnterURL':'Please enter an URL',
101
'videoURLnotSupported':'Video URL not supported',
102
'pleaseSelectImage':'Please select an image',
103
'pleaseSelectFile':'Please select a file',
104
'bold':'Bold',
105
'italic':'Italic',
106
'underline':'Underline',
107
'alignLeft':'Align left',
108
'alignCenter':'Align centered',
109
'alignRight':'Align right',
110
'addOrderedList':'Add ordered list',
111
'addUnorderedList':'Add unordered list',
112
'addHeading':'Add Heading/title',
113
'addFont':'Add font',
114
'addFontColor':'Add font color',
115
'addFontSize':'Add font size',
116
'addImage':'Add image',
117
'addVideo':'Add video',
118
'addFile':'Add file',
119
'addURL':'Add URL',
120
'addTable':'Add table',
121
'removeStyles':'Remove styles',
122
'code':'Show HTML code',
123
'undo':'Undo',
124
'redo':'Redo',
125
'close':'Close'
126
},
127

128
// privacy
129
youtubeCookies:false,
130

131
// dev settings
132
useSingleQuotes:false,
133
height: 0,
134
heightPercentage: 0,
135
id:"",
136
class:"",
137
useParagraph:false,
138
maxlength: 0,
139

140
// callback function after init
141
callback: undefined
142
});
