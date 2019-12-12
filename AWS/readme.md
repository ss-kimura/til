### EC2
- EC2のinbound ruleだけ開けてもダメ。firewall-cmdでもポートを開ける必要がある
- 停止と終了は全然違う・・。定期的にOSイメージのAMIを作るか、EBSのスナップショットを作っておけば、間違えて終了しても復元できる。
- Terminate Protectionをかけるか、権限ない人はterminateできないようにすべき。

### S3
```php
$this->config = [
    'key'    => $this->accessKey,
    'secret' => $this->secretKey,
    'region' => $this->region,
    'version' => 'latest',
];
```

composerでいれたaws-sdkのversionによって  
```Error retrieving credentials from the instance profile metadata server```
こんなエラーになるので、
```php
$this->config = [
    'region' => $this->region,
    'version' => 'latest',
    'credentials' => [
        'key' => $this->accessKey,
        'secret' => $this->secretKey,
     ],
];
```
