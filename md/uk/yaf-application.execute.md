---
navigation:
  - yaf-application.environ.md: '« Yaf\_Application::environ'
  - yaf-application.getappdirectory.md: 'Yaf\_Application::getAppDirectory »'
  - index.md: PHP Manual
  - class.yaf-application.md: Yaf\_Application
title: 'Yaf\_Application::execute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Application::execute

(Yaf >=1.0.0)

Yaf\_Application::execute — Запустити callback-функцію

### Опис

```methodsynopsis
public Yaf_Application::execute(callable $entry, string ...$args): void
```

Цей метод зазвичай використовується для запуску Yaf\_Application через планувальник (crontab). Завдання crontab також може використовувати механізми autoloader і Bootstrap.

### Список параметрів

`entry`

Callback-функція

`args`

Параметри, які потрібно передати в цю функцію

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** Yaf\_Application::execute()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:
