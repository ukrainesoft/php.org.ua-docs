---
navigation:
  - yaf-application.getlasterrorno.md: '« Yaf\_Application::getLastErrorNo'
  - yaf-application.run.md: 'Yaf\_Application::run »'
  - index.md: PHP Manual
  - class.yaf-application.md: Yaf\_Application
title: 'Yaf\_Application::getModules'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Application::getModules

(Yaf >=1.0.0)

Yaf\_Application::getModules — Отримати імена заявлених модулів

### Опис

```methodsynopsis
public Yaf_Application::getModules(): array
```

Отримати список модулів, заданих у конфігураційному файлі. Якщо жодного модуля не встановлено, то у вашому розпорядженні завжди є модуль "Index".

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** Yaf\_Application::getModules()\*\*\*\*

```php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
print_r($application->getModules());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => Index
)
```
