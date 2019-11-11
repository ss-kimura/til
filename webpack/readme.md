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

# 開発環境構築

1. Install webpack globally  
```npm install -g webpack```

2. create a package.json file  
```npm init -y```  
