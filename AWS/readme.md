### EC2
- EC2のinbound ruleだけ開けてもダメ。firewall-cmdでもポートを開ける必要がある

### s3
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
