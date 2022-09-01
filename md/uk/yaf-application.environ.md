---
navigation:
  - yaf-application.destruct.html: '« YafApplication::destruct'
  - yaf-application.execute.html: 'YafApplication::execute »'
  - index.md: PHP Manual
  - class.yaf-application.html: YafApplication
title: 'YafApplication::environ'
---
# YafApplication::environ

(Yaf >=1.0.0)

YafApplication::environ — Отримати значення оточення

### Опис

```methodsynopsis
public Yaf_Application::environ(): void
```

Отримати значення оточення з yaf.environ, яке за умовчанням дорівнює "product".

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafApplication::environ()****

```php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
print_r($application->environ());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
product
```
