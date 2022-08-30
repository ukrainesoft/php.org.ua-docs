Реєструє простір імен шляхом пошуку

-   [« YafLoader::registerLocalNamespace](yaf-loader.registerlocalnamespace.html)
    
-   [YafLoader::setLibraryPath »](yaf-loader.setlibrarypath.html)
    
-   [PHP Manual](index.md)
    
-   [YafLoader](class.yaf-loader.html)
    
-   Реєструє простір імен шляхом пошуку
    

# YafLoader::registerNamespace

(Yaf> = 3.2.0)

YafLoader::registerNamespace — Реєструє простір імен шляхом пошуку

### Опис

```methodsynopsis
public Yaf_Loader::registerNamespace(string|array $namespaces, string $path = ?): bool
```

Реєструє простір імен шляхом пошуку, [YafLoader](class.yaf-loader.html) шукає класи в цьому просторі імен у дорозі, він також може бути налаштований за допомогою [application.library.directory.namespace](yaf.appconfig.html#configuration.yaf.library.namespace)(application.ini);

> **Зауваження**
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

**Приклад #1 Приклад використання **YafLoader::registerNamespace()****

```php
<?php
$loader = Yaf_Loader::getInstance();
$loader->registerNamespace("\Vendor\PHP", "/var/lib/php");
$loader->registerNamespace(array(
     "\Vendor\ASP" => "/var/lib/asp",
     "\Vendor\JSP" => "/usr/lib/vendor/",
));

$loader->autoload("\Vendor\PHP\Dummy");   //load '/var/lib/php/Dummy.php'
$loader->autoload("\Vendor\PHP\Foo_Bar"); //load '/var/lib/php/Foo/Bar.php'
$loader->autoload("\Vendor\JSP\Dummy");   //load '/usr/lib/vendor/Dummy.php'

?>
```