- jsにデータを渡すとき、json_encodeはphp側ではなく、js側でやる。php側でやると&quot;が混ざる
```javascript
var a = JSON.parse('<?php echo json_encode($something, JSON_UNESCAPED_UNICODE); ?>');
```
