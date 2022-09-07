---
navigation:
  - yaf-application.environ.md: '« YafApplication::environ'
  - yaf-application.getappdirectory.md: 'YafApplication::getAppDirectory »'
  - index.md: PHP Manual
  - class.yaf-application.md: YafApplication
title: 'YafApplication::execute'
---
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
function main($argc, $argv) {
}

$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
$application->execute("main", $argc,  $argv);
?>
```

Результатом виконання цього прикладу буде щось подібне:
