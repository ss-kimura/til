JSの役割が大きくなるにつれ、コード量が増え複雑になってきてるが、

例えば、

```<script src="module1.js"></script>```  
```<script src="module2.js"></script>```
```<script src="module3.js"></script>```

のように連続で読み込んだ場合、ローディング順序によって変数のスコープが衝突したり、同じ変数の中身が上書きされたり、
複雑なので管理しにくい

⇒ このような問題を解決するためにwebpackが登場

# webpackの哲学
- Everything is Module すべてのリソース(js, css, html)がモジュール形式でローディング可  
```require('style.css')```  
```require('main.js')```

- Load only what you need and when you need 必要時、必要なもののみローディングして使用する

# UNPKG  
インストールなしで使えるnpmライブラリ
```unpkg.com/:package@:version/:file```

# 開発環境構築
1. make js-test directory and move the directory  

2. Install webpack globally  
```npm install -g webpack@3.6```

3. create a package.json file  
```npm init -y```  

4. install lodash library  
```npm i lodash --save```  
--saveはdefendenciesに追記してくれる

5. create index.js file  
```javascript
import _ from 'lodash';

function component() {
    var element = document.createElement('div');

    element.innerHTML = _.join(['hello', 'webpack'], ' ');

    return element;
}
document.body.appendChild(component());
```

6. create index.html  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    <script src="app/index.js"></script>    
</body>
</html>
```

7. bundling with webpack  
```webpack app/index.js dist/bundle.js```  
bundle.jsができあがるので、今後はこれをローディングする。  
jsファイルを何度もローディングしなくてもいい。

8. create webpack.config.js  
webpackコマンドをいちいち打つのではなくwebpack.config.jsファイルに定義しておくと便利
```javascript
var path = require('path');

module.exports = {
    entry: './app/index.js',
    output: {
        filename: 'bundle.js',
        path: path.resolve(__dirname, 'dist')
    }
};
```
上記を定義しておけば、webpackと打つだけでいい
