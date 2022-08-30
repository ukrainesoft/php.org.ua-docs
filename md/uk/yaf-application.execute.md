Запустити callback-функцію

-   [« YafApplication::environ](yaf-application.environ.html)
    
-   [YafApplication::getAppDirectory »](yaf-application.getappdirectory.html)
    
-   [PHP Manual](index.html)
    
-   [YafApplication](class.yaf-application.html)
    
-   Запустити callback-функцію
    

# YafApplication::execute

(Yaf >=1.0.0)

YafApplication::execute — Запустити callback-функцію

### Опис

```methodsynopsis
public Yaf_Application::execute(callable $entry, string ...$args): void
```

Цей метод зазвичай використовується для запуску YafApplication через планувальник (crontab). Завдання crontab також може використовувати механізми autoloader і Bootstrap.

### Список параметрів

`entry`

Callback-функція

`args`

Параметри, які потрібно передати в цю функцію

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafApplication::execute()****

```php
<?php
function main($argc, $argv) {
}

$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
$application->execute("main", $argc,  $argv);
?>
```

Результатом виконання цього прикладу буде щось подібне: