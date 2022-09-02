---
navigation:
  - yaf-loader.getlocalnamespace.md: '« YafLoader::getLocalNamespace'
  - yaf-loader.getnamespaces.md: 'YafLoader::getLocalNamespace »'
  - index.md: PHP Manual
  - class.yaf-loader.md: YafLoader
title: 'YafLoader::getNamespacePath'
---
# YafLoader::getNamespacePath

(Yaf> = 3.2.0)

YafLoader::getNamespacePath — Отримує шлях зареєстрованого простору імен

### Опис

```methodsynopsis
public Yaf_Loader::getNamespacePath(string $namespaces): string
```

Отримує шлях зареєстрованого простору імен

### Список параметрів

`namespace`

Рядок простору імен.

### Значення, що повертаються

string шлях, якщо простір імен не зареєстрований, то поверне **`null`**. Буде повернуто бібліотеку за замовчуванням.

### Приклади

**Приклад #1 Приклад використання [YafLoader::registerNamespace()](yaf-loader.registernamespace.md)**

```php
<?php
$loader = Yaf_Loader::getInstance("/var/application/lib");
$loader->registerNamespace("\Vendor\PHP", "/var/lib/php");

$loader->getNamespacePath("\Vendor\PHP"); // '/var/lib/php'
$loader->getNamespacePath("\Vendor\JSP"); // '/var/application/lib'

?>
```
