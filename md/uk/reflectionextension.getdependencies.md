Отримання залежностей

-   [« ReflectionExtension::getConstants](reflectionextension.getconstants.html)
    
-   [ReflectionExtension::getFunctions »](reflectionextension.getfunctions.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionExtension](class.reflectionextension.html)
    
-   Отримання залежностей
    

# ReflectionExtension::getDependencies

(PHP 5> = 5.1.3, PHP 7, PHP 8)

ReflectionExtension::getDependencies — Отримання залежностей

### Опис

```methodsynopsis
public ReflectionExtension::getDependencies(): array
```

Отримує список необхідних та конфліктуючих залежностей.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив array, ключами якого є залежності, а значеннями є наступні рядки: `Required` `Optional` або `Conflicts`

### Приклади

**Приклад #1 Приклад використання **ReflectionExtension::getDependencies()****

```php
<?php
$dom = new ReflectionExtension('dom');

print_r($dom->getDependencies());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [libxml] => Required
    [domxml] => Conflicts
)
```

### Дивіться також

-   **ReflectionClass::getVersion()**