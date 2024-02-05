---
navigation:
  - yaf-loader.registerlocalnamespace.md: '« Yaf\_Loader::registerLocalNamespace'
  - yaf-loader.setlibrarypath.md: 'Yaf\_Loader::setLibraryPath »'
  - index.md: PHP Manual
  - class.yaf-loader.md: Yaf\_Loader
title: 'Yaf\_Loader::registerNamespace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Loader::registerNamespace

(Yaf >=3.2.0)

Yaf\_Loader::registerNamespace — Реєструє простір імен шляхом пошуку

### Опис

```methodsynopsis
public Yaf_Loader::registerNamespace(string|array $namespaces, string $path = ?): bool
```

Реєструє простір імен шляхом пошуку, [Yaf\_Loader](class.yaf-loader.md) шукає класи в цьому просторі імен у дорозі, він також може бути налаштований за допомогою [application.library.directory.namespace](yaf.appconfig.md#configuration.yaf.library.namespace)(application.ini);

> **Зауваження** :
> 
> Yaf все ще розглядає, підкреслення як роздільник папок.

### Список параметрів

`namespace`

рядок простору імен або масив просторів імен із шляхами.

`path`

рядок шляху, краще використовувати абсолютний шлях для продуктивності

### Значення, що повертаються

bool

### Приклади

**Пример #1 Пример использования**Yaf\_Loader::registerNamespace()\*\*\*\*

```php
<?php
$loader = Yaf_Loader::getInstance();
$loader->registerNamespace("\Vendor\PHP", "/var/lib/php");
$loader->registerNamespace(array(
     "\Vendor\ASP" => "/var/lib/asp",
     "\Vendor\JSP" => "/usr/lib/vendor/",
));

$loader->autoload("\Vendor\PHP\Dummy");   //load '/var/lib/php/Dummy.php'
$loader->autoload("\Vendor\PHP\Foo_Bar"); //load '/var/lib/php/Foo/Bar.php'
$loader->autoload("\Vendor\JSP\Dummy");   //load '/usr/lib/vendor/Dummy.php'

?>
```
