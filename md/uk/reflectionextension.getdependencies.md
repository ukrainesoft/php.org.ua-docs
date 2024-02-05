---
navigation:
  - reflectionextension.getconstants.md: '« ReflectionExtension::getConstants'
  - reflectionextension.getfunctions.md: 'ReflectionExtension::getFunctions »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::getDependencies'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionExtension::getDependencies

(PHP 5 >= 5.1.3, PHP 7, PHP 8)

ReflectionExtension::getDependencies — Отримання залежностей

### Опис

```methodsynopsis
public ReflectionExtension::getDependencies(): array
```

Отримує список необхідних та конфліктуючих залежностей.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив array, ключами якого є залежності, а значеннями є наступні рядки: `Required` `Optional`или`Conflicts`

### Приклади

**Пример #1 Пример использования**ReflectionExtension::getDependencies()\*\*\*\*

```php
<?php
$dom = new ReflectionExtension('dom');

print_r($dom->getDependencies());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [libxml] => Required
    [domxml] => Conflicts
)
```

### Дивіться також

-   **ReflectionClass::getVersion()**
