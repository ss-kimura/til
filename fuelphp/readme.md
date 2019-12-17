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
```FUEL_ENV=localhost php oil refine test``` or ```FUEL_ENV=localhost php oil refine test:get "something"```  
apiやcmsと違い、サーバーを通さないので環境変数を指定しないといけない

# crontab
```0 19 * * *  FUEL_ENV=development  /usr/bin/php /var/xxx/oil refine blog```  

