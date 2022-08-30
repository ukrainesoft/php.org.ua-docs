Отримати підтримувані локалі

-   [« ResourceBundle::get](resourcebundle.get.html)
    
-   [Spoofchecker »](class.spoofchecker.html)
    
-   [PHP Manual](index.html)
    
-   [ResourceBundle](class.resourcebundle.html)
    
-   Отримати підтримувані локалі
    

# ResourceBundle::getLocales

# resourcebundlelocales

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL intl >= 2.0.0)

ResourceBundle::getLocales -- resourcebundlelocales — Отримати підтримувані локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static ResourceBundle::getLocales(string $bundle): array|false
```

Процедурний стиль

```methodsynopsis
resourcebundle_locales(string $bundle): array|false
```

Повертає доступні в ResourceBundle локалі.

### Список параметрів

`bundle`

Шлях до ResourceBundle або порожній рядок для отримання списку за замовчуванням або **`false`** у разі виникнення помилки.

### Значення, що повертаються

Повертає доступні в ResourceBundle локалі.

### Приклади

**Приклад #1 Приклад використання **resourcebundlelocales()****

```php
<?php
$bundle = "/user/share/data/myapp";
echo join(PHP_EOL, resourcebundle_locales($bundle));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
es
root
```

**Приклад #2 Приклад в об'єктно-орієнтованому стилі**

```php
<?php
$bundle = "/usr/share/data/myapp";
$r = new ResourceBundle( 'es', $bundle);
echo join("\n", $r->getLocales($bundle));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
es
root
```

### Дивіться також

-   [resourcebundleget()](resourcebundle.get.html) - Отримати дані з пакета