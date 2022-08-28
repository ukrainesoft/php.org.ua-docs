Отримати значення оточення

-   [« Yaf\_Application::\_\_destruct](yaf-application.destruct.html)
    
-   [Yaf\_Application::execute »](yaf-application.execute.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Application](class.yaf-application.html)
    
-   Отримати значення оточення
    

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