# Inline Style  
HTML要素に直接CSSを記述。**使うべきでない**が、デバック時は使ったりする。  
```<div style="color:red;">text</div>```  

# Embedded Style  
styleタグに生で書く。ページ数が増えた時、変更が大変なので**使うべきでない**。  
```
<head>
<style>
.b {
  color:blue;
}
</style>
</head>
<body>
<div class="b">text</div>
```

# Linked Style  
割と良く使う
```<link rel="stylesheet" type="text/css" href="some.css">```  

# Import Style  
```@import url('some.css');```  
styleタグに書くこともできるが、Embedded Style同様、メンテナンスが大変なので  
CSSファイルの中で使うべき。CSSファイルにそのままIncludeする。  

# 書き方  
セレクタ { 属性: 値; }  
div { font-size: 10px; }  

# セレクタ優先順位
