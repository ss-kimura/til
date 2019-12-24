- jsにデータを渡すとき、json_encodeはphp側ではなく、js側でやる。php側でやると&quot;が混ざる
```javascript
var a = JSON.parse('<?php echo json_encode($something, JSON_UNESCAPED_UNICODE); ?>');
```
- メールアドレスチェック  
```php
private static function checkEmail($email) {
    switch ($email) {
        case !filter_var($email, FILTER_VALIDATE_EMAIL):
        case !preg_match("/^([a-zA-Z0-9])+([a-zA-Z0-9\._-])*@([a-zA-Z0-9_-])+([a-zA-Z0-9\._-]+)+$/", $email):
            return false;
        default:
            return true;
    }
}
```
