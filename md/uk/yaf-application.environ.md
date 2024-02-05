---
navigation:
  - yaf-application.destruct.md: '« Yaf\_Application::\_\_destruct'
  - yaf-application.execute.md: 'Yaf\_Application::execute »'
  - index.md: PHP Manual
  - class.yaf-application.md: Yaf\_Application
title: 'Yaf\_Application::environ'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Application::environ

(Yaf >=1.0.0)

Yaf\_Application::environ — Отримати значення оточення

### Опис

```methodsynopsis
public Yaf_Application::environ(): void
```

Отримати значення оточення з yaf.environ, яке за умовчанням дорівнює "product".

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Yaf\_Application::environ()\*\*\*\*

```php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
print_r($application->environ());
?>
```

Висновок наведеного прикладу буде схожим на:

```
product
```
