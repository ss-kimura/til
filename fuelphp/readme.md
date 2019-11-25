# cron処理
fuel/app/tasksに処理を記述  
```php
<?php
namespace Fuel\Tasks;
use Fuel\Core\Cli;
use Fuel\Core\DB;
use Fuel\Core\DBUtil;
use Curl\CurlUtil;

class Test
{
    public function run()
    {
        echo "処理";
    }

    public function get($some = "something")
    {
        echo $some;
    }
}
```

# 実行
```php oil refine test``` or ```php oil refine test:get "something"```  

# crontab
```* * * * * php /some_path/oil refine test```

