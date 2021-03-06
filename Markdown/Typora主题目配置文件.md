**该配置文件使用了其自带的 Catfish 和 Gothic 的字符文件，所以使用前需安装这两个主题。**
```css
@include-when-export url(http://fonts.googleapis.com/css?family=Ubuntu:400,700,400italic,700italic);
@include-when-export url(http://fonts.googleapis.com/css?family=Raleway:600,400&subset=latin,latin-ext);
@charset "UTF-8";
@font-face {
    font-family: 'TeXGyreAdventor';
    src: url('texgyreadventor-regular.otf');
    font-weight: normal;
    font-style: normal;

}

@charset "UTF-8";
@font-face {
	font-family: 'TeXGyreAdventor';
	font-style: normal;
	font-weight: normal;
	src: url(./gothic/texgyreadventor-regular.otf);
}
@font-face {
	font-family: 'TeXGyreAdventor';
	font-style: normal;
	font-weight: bold;
	src: url(./gothic/texgyreadventor-bold.otf);
}
@font-face {
	font-family: 'TeXGyreAdventor';
	font-style: italic;
	font-weight: normal;
	src: url(./gothic/texgyreadventor-italic.otf);
}
@font-face {
	font-family: 'TeXGyreAdventor';
	font-style: italic;
	font-weight: bold;
	src: url(./gothic/texgyreadventor-bolditalic.otf);
}
@font-face {
  font-family: Source Han Sans;
  font-weight: normal;
  src: local('Source Han Sans Regular'), url("catfish/SourceHanSans-Regular.ttc");
}
@font-face {
  font-family: Source Han Sans;
  font-weight: bold;
  src: local('Source Han Sans Bold'), url("catfish/SourceHanSans-Bold.ttc");
}
@font-face {
  font-family: Source Han Serif;
  font-weight: normal;
  src: local('Source Han Serif Regular'), url("catfish/SourceHanSerif-Regular.ttc");
}
@font-face {
  font-family: Source Han Serif;
  font-weight: bold;
  src: local('Source Han Serif Bold'), url("catfish/SourceHanSerif-Bold.ttc");
}
@font-face {
  font-family: mononoki;
  font-style: normal;
  font-weight: normal;
  src: local('mononoki Regular'), url("catfish/mononoki-Regular.woff");
}
@font-face {
  font-family: mononoki;
  font-style: italic;
  font-weight: normal;
  src: local('mononoki Italic'), url("catfish/mononoki-Italic.woff");
}
@font-face {
  font-family: mononoki;
  font-style: normal;
  font-weight: bold;
  src: local('mononoki Bold'), url("catfish/mononoki-Bold.woff");
}
@font-face {
  font-family: mononoki;
  font-style: italic;
  font-weight: bold;
  src: local('mononoki Bold Italic'), url("catfish/mononoki-BoldItalic.woff");
}

html,
body,
#write{
	background: #fcfcfc;
	/*font-family: 'TeXGyreAdventor', "Century Gothic", 'Yu Gothic', 'Raleway', "STHeiti", sans-serif;*/
    font-family: 'TeXGyreAdventor', Source Han Sans, Noto, Helvetica Neue, Helvetica, PingFang SC, Hiragino Sans GB, Microsoft YaHei, WenQuanYi Micro Hei, Arial, sans-serif;
	font-weight: 400;
}
h1,
h2,
h3,
h4,
h5,
h6 {
	color: #111;
    font-family: 'TeXGyreAdventor', Source Han Sans, Noto, Helvetica Neue, Helvetica, PingFang SC, Hiragino Sans GB, Microsoft YaHei, WenQuanYi Micro Hei, Arial, sans-serif;
	/*font-family: 'TeXGyreAdventor', "Century Gothic", 'Yu Gothic', 'Ubuntu', "STHeiti", sans-serif;*/
}

html {
	font-size:16px;
}

#write {
	max-width: 914px;
	text-align: justify;
}

#write>h1:first-child {
	margin-top: 2.75rem;
}
#write>h2:first-child {
	margin-top: 1.75rem;
}
#write>h3:first-child {
	margin-top: 1rem;
}
#write>h4:first-child {
	margin-top: 0.5rem;
}
h1 {
	font-weight: normal;
	line-height: 4rem;
	margin: 0 0 1.75rem;
	<!-- padding: 20px 30px; -->
	<!-- text-align: center; -->
	text-transform: uppercase;
	margin-top: 4rem;
}
h2 {
	font-weight: normal;
	line-height: 3rem;
	margin: 0 0 1.9375rem;
	<!-- padding: 0 30px; -->
	<!-- text-align: center; -->
	text-transform: uppercase;
	margin-top: 3rem
}
h3 {
	font-weight: normal;
}
h4 {
	font-weight: normal;
}
h5 {
	font-size: 1.125rem;
	font-weight: normal;
}
h6 {
	font-size: 1rem;
	font-weight: bold;
}
p {
	color: #111;
	font-size: 1rem;
    /*line-height: 1.75rem;*/
    line-height: 1.50rem;
	/*margin: 0 0 1.25rem;*/
	margin: 0 0 0.75rem;
}
#write>h3.md-focus:before {
	left: -1.875rem;
	top: 0.5rem;
	padding: 2px;
}
#write>h4.md-focus:before {
	left: -1.875rem;
	top: 0.3125rem;
	padding: 2px;
}
#write>h5.md-focus:before {
	left: -1.875rem;
	top: 0.25rem;
	padding: 2px;
}
#write>h6.md-focus:before {
	left: -1.875rem;
	top: .125rem;
	padding: 2px;
}
/*@media screen and (min-width: 48em) {
	.h1,
	h1 {
		font-size: 3.250rem;
	}
	.h2,
	h2 {
		font-size: 2.298rem;
	}
	.h3,
	h3 {
		font-size: 1.625rem;
	}
	.h4,
	h4 {
		font-size: 1.250rem;
	}
	.h5,
	h5 {
		font-size: 1.150rem;
	}
	.h6,
	h6 {
		font-size: 1rem;
	}
	#write>h4.md-focus:before,
	#write>h5.md-focus:before,
	#write>h6.md-focus:before {
		top: 1px;
	}
	p {
		font-size: 1.25rem;
		line-height: 1.8;
	}
	table {
		font-size: 1.25rem;
	}
}*/
@media screen and (max-width: 48em) {
	blockquote {
		margin-left: 1rem;
		margin-right: 0;
		padding: 0.5em;
	}
	.h1,
	h1 {
		font-size: 2.827rem;
	}
	.h2,
	h2 {
		font-size: 1.999rem;
	}
	.h3,
	h3 {
		font-size: 1.413rem;
	}
	.h4,
	h4 {
		font-size: 1.250rem;
	}
	.h5,
	h5 {
		font-size: 1.150rem;
	}
	.h6,
	h6 {
		font-size: 1rem;
	}
}
a,
.md-def-url {
	color: #990000;
	text-decoration: none;
}
a:hover {
	text-decoration: underline;
}
table {
	margin-bottom: 20px
}
table th,
table td {
	padding: 8px;
	line-height: 1.25rem;
	vertical-align: top;
	border-top: 1px solid #ddd
}
table th {
	font-weight: bold
}
table thead th {
	vertical-align: bottom
}
table caption+thead tr:first-child th,
table caption+thead tr:first-child td,
table colgroup+thead tr:first-child th,
table colgroup+thead tr:first-child td,
table thead:first-child tr:first-child th,
table thead:first-child tr:first-child td {
	border-top: 0
}
table tbody+tbody {
	border-top: 2px solid #ddd
}
code, .md-fences {
	padding: .5em;
	/*background: #f0f0f0;*/
	border: 1px solid #ccc;
	padding: .1em;
	font-size: 0.9em;
	margin-left: 0.2em;
	margin-right: 0.2em;
}
.md-fences {
	margin: 0 0 20px;
	font-size: 1em;
	padding: 0.3em 1em;
  	padding-top: 0.4em;
}
.task-list{
	padding-left: 0;
}

.task-list-item {
	padding-left:2.125rem;
}

.task-list-item input {
	top: 3px;

}

.task-list-item input:before {
	content: "";
	display: inline-block;
	width: 1rem;
	height: 1rem;
	vertical-align: middle;
	text-align: center;
	border: 1px solid gray;
	background-color: #fdfdfd;
	margin-left: 0;
	margin-top: -0.8rem;
}
.task-list-item input:checked:before,
.task-list-item input[checked]:before{
	content: '\25FC';
	/*◘*/
	font-size: 0.8125rem;
	line-height: 0.9375rem;
	margin-top: -1rem;
}

/* Chrome 29+ */
@media screen and (-webkit-min-device-pixel-ratio:0)
  and (min-resolution:.001dpcm) {
    .task-list-item input:before {
    	margin-top: -0.2rem;
    }

    .task-list-item input:checked:before,
	.task-list-item input[checked]:before {
		margin-top: -0.2rem;
	}
}

blockquote {
	margin: 0 0 1.11111rem;
	padding: 0.5rem 1.11111rem 0 1.05556rem;
    font-family: Source Han Serif, Noto Serif, serif;
	border-left: 1px solid gray;
}
blockquote,
blockquote p {
	line-height: 1.6;
	/*line-height: 1.2;*/
	color: #6f6f6f;
}
#write pre.md-meta-block {
	min-height: 30px;
	background: #f8f8f8;
	padding: 1.5em;
	font-weight: 300;
	font-size: 1em;
	padding-bottom: 1.5em;
	padding-top: 3em;
    margin-top: -1.5em;
	color: #999;
	border-left: 1000px #f8f8f8 solid;
	margin-left: -1000px;
	border-right: 1000px #f8f8f8 solid;
	margin-right: -1000px;
	margin-bottom: 2em;
}
.MathJax_Display {
	font-size: 0.9em;
	margin-top: 0.5em;
	margin-bottom: 0;
}
p.mathjax-block,
.mathjax-block {
	padding-bottom: 0;
}
.mathjax-block>.code-tooltip {
	bottom: 5px;
	box-shadow: none;
}
.md-image>.md-meta {
	padding-left: 0.5em;
	padding-right: 0.5em;
}
.md-image>img {
	margin-top: 2px;
}
.md-image>.md-meta:first-of-type:before {
	padding-left: 4px;
}

#typora-source {
	color: #555;
}

/** ui for windows **/
#md-searchpanel {
    border-bottom: 1px solid #ccc;
}

#md-searchpanel .btn {
    border: 1px solid #ccc;
}

#md-notification:before {
	top: 14px;
}

#md-notification {
	background: #eee;
}

.megamenu-menu-panel .btn {
	border: 1px solid #ccc;
}
```
