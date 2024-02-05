---
navigation:
  - yaf-loader.getlocalnamespace.md: '« Yaf\_Loader::getLocalNamespace'
  - yaf-loader.getnamespaces.md: 'Yaf\_Loader::getLocalNamespace »'
  - index.md: PHP Manual
  - class.yaf-loader.md: Yaf\_Loader
title: 'Yaf\_Loader::getNamespacePath'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Loader::getNamespacePath

(Yaf >=3.2.0)

Yaf\_Loader::getNamespacePath — Отримує шлях зареєстрованого простору імен

### Опис

```methodsynopsis
public Yaf_Loader::getNamespacePath(string $namespaces): string
```

Отримує шлях зареєстрованого простору імен

### Список параметрів

`namespace`

Рядок простору імен.

### Значення, що повертаються

string шлях, якщо простір імен не зареєстрований, то поверне \*\*`null`\*\*Будет возвращена библиотека по умолчанию.

### Приклади

**Приклад #1 Приклад использования[Yaf\_Loader::registerNamespace()](yaf-loader.registernamespace.md)**

```php
<?php
$loader = Yaf_Loader::getInstance("/var/application/lib");
$loader->registerNamespace("\Vendor\PHP", "/var/lib/php");

$loader->getNamespacePath("\Vendor\PHP"); // '/var/lib/php'
$loader->getNamespacePath("\Vendor\JSP"); // '/var/application/lib'

?>
```
