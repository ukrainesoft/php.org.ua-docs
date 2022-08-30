Отримати останній код помилки пакета

-   [« ResourceBundle::create](resourcebundle.create.md)
    
-   [ResourceBundle::getErrorMessage »](resourcebundle.geterrormessage.md)
    
-   [PHP Manual](index.md)
    
-   [ResourceBundle](class.resourcebundle.md)
    
-   Отримати останній код помилки пакета
    

# ResourceBundle::getErrorCode

# resourcebundlegeterrorcode

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL intl >= 2.0.0)

ResourceBundle::getErrorCode -- resourcebundlegeterrorcode — Отримати останній код помилки пакета

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public ResourceBundle::getErrorCode(): int
```

Процедурний стиль

```methodsynopsis
resourcebundle_get_error_code(ResourceBundle $bundle): int
```

Повертає код останньої помилки, що виникла при виклику функцій пакета.

### Список параметрів

`bundle`

Об'єкт [ResourceBundle](class.resourcebundle.md)

### Значення, що повертаються

Повертає код останньої помилки, що виникла при виклику функцій пакета.

### Приклади

**Приклад #1 Приклад використання **resourcebundlegeterrorcode()****

```php
<?php
$r = resourcebundle_create( 'es', "/usr/share/data/myapp");
echo $r['somestring'];
if(intl_is_failure(resourcebundle_get_error_code($r))) {
    report_error("Ошибка пакета");
}
?>
```

**Приклад #2 Приклад в об'єктно-орієнтованому стилі**

```php
<?php
$r = new ResourceBundle( 'es', "/usr/share/data/myapp");
echo $r['somestring'];
if(intl_is_failure(ResourceBundle::getErrorCode($r))) {
    report_error("Ошибка пакета");
}
?>
```

### Дивіться також

-   [resourcebundlegeterrormessage()](resourcebundle.geterrormessage.md) - Отримати останнє повідомлення про помилку пакета
-   [intlgeterrorcode()](function.intl-get-error-code.html) - Отримати код останньої помилки
-   [intlісfailure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою