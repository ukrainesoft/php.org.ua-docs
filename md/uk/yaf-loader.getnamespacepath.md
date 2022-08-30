Отримує шлях зареєстрованого простору імен

-   [« YafLoader::getLocalNamespace](yaf-loader.getlocalnamespace.html)
    
-   [YafLoader::getLocalNamespace »](yaf-loader.getnamespaces.html)
    
-   [PHP Manual](index.md)
    
-   [YafLoader](class.yaf-loader.html)
    
-   Отримує шлях зареєстрованого простору імен
    

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

**Приклад #1 Приклад використання [YafLoader::registerNamespace()](yaf-loader.registernamespace.html)**

```php
<?php
$loader = Yaf_Loader::getInstance("/var/application/lib");
$loader->registerNamespace("\Vendor\PHP", "/var/lib/php");

$loader->getNamespacePath("\Vendor\PHP"); // '/var/lib/php'
$loader->getNamespacePath("\Vendor\JSP"); // '/var/application/lib'

?>
```