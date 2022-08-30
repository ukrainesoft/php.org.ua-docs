Приклади

-   [« Обумовлені константи](xhprof.constants.md)
    
-   [Функции Xhprof »](ref.xhprof.md)
    
-   [PHP Manual](index.md)
    
-   [Xhprof](book.xhprof.md)
    
-   Приклади
    

# Приклади

**Приклад #1 Приклади використання Xhprof, опціонально з GUI**

У цьому прикладі профайлер запускається, зупиняється та використовує вбудований GUI інтерфейс для збереження та аналізу результатів. Іншими словами, виконання коду модуля завершується на функції [xhprofdisable()](function.xhprof-disable.html)

```php
<?php
xhprof_enable(XHPROF_FLAGS_CPU + XHPROF_FLAGS_MEMORY);

for ($i = 0; $i <= 1000; $i++) {
    $a = $i * $i;
}

$xhprof_data = xhprof_disable();

$XHPROF_ROOT = "/tools/xhprof/";
include_once $XHPROF_ROOT . "/xhprof_lib/utils/xhprof_lib.php";
include_once $XHPROF_ROOT . "/xhprof_lib/utils/xhprof_runs.php";

$xhprof_runs = new XHProfRuns_Default();
$run_id = $xhprof_runs->save_run($xhprof_data, "xhprof_testing");

echo "http://localhost/xhprof/xhprof_html/index.php?run={$run_id}&source=xhprof_testing\n";

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
http://localhost/xhprof/xhprof_html/index.php?run=t11_4bdf44d21121f&source=xhprof_testing
```