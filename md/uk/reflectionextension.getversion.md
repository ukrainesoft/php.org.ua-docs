Отримання версії модуля

-   [« ReflectionExtension::getName](reflectionextension.getname.html)
    
-   [ReflectionExtension::info »](reflectionextension.info.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionExtension](class.reflectionextension.html)
    
-   Отримання версії модуля
    

# ReflectionExtension::getVersion

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::getVersion — Отримання версії модуля

### Опис

```methodsynopsis
public ReflectionExtension::getVersion(): ?string
```

Отримує версію модуля.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Версія модуля, або **`null`** якщо модуль не має версії.

### Приклади

**Приклад #1 Приклад використання **ReflectionExtension::getVersion()****

```php
<?php
$ext = new ReflectionExtension('mysqli');
var_dump($ext->getVersion());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(3) "0.1"
```

### Дивіться також

-   [ReflectionExtension::info()](reflectionextension.info.html) - Виведення інформації про модуль