Отримати імена заявлених модулів

-   [« Yaf\_Application::getLastErrorNo](yaf-application.getlasterrorno.html)
    
-   [Yaf\_Application::run »](yaf-application.run.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Application](class.yaf-application.html)
    
-   Отримати імена заявлених модулів
    

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