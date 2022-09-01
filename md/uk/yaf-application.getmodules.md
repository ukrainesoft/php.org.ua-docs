---
navigation:
  - yaf-application.getlasterrorno.html: '« YafApplication::getLastErrorNo'
  - yaf-application.run.html: 'YafApplication::run »'
  - index.md: PHP Manual
  - class.yaf-application.html: YafApplication
title: 'YafApplication::getModules'
---
# YafApplication::getModules

(Yaf >=1.0.0)

YafApplication::getModules — Отримати імена заявлених модулів

### Опис

```methodsynopsis
public Yaf_Application::getModules(): array
```

Отримати список модулів, заданих у конфігураційному файлі. Якщо жодного модуля не встановлено, то у вашому розпорядженні завжди є модуль "Index".

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafApplication::getModules()****

```php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
print_r($application->getModules());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => Index
)
```
