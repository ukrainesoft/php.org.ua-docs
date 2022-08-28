Отримати останній код помилки пакета

-   [« ResourceBundle::create](resourcebundle.create.html)
    
-   [ResourceBundle::getErrorMessage »](resourcebundle.geterrormessage.html)
    
-   [PHP Manual](index.html)
    
-   [ResourceBundle](class.resourcebundle.html)
    
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

Об'єкт [ResourceBundle](class.resourcebundle.html)

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

-   [resourcebundle\_get\_error\_message()](resourcebundle.geterrormessage.html) - Отримати останнє повідомлення про помилку пакета
-   [intl\_get\_error\_code()](function.intl-get-error-code.html) - Отримати код останньої помилки
-   [intl\_is\_failure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою