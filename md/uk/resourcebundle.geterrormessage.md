Отримати останнє повідомлення про помилку пакету

-   [« ResourceBundle::getErrorCode](resourcebundle.geterrorcode.html)
    
-   [ResourceBundle::get »](resourcebundle.get.html)
    
-   [PHP Manual](index.html)
    
-   [ResourceBundle](class.resourcebundle.html)
    
-   Отримати останнє повідомлення про помилку пакету
    

# ResourceBundle::getErrorMessage

# resourcebundlegeterrormessage

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL intl >= 2.0.0)

ResourceBundle::getErrorMessage -- resourcebundlegeterrormessage — Отримати останнє повідомлення про помилку пакета

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public ResourceBundle::getErrorMessage(): string
```

Процедурний стиль

```methodsynopsis
resourcebundle_get_error_message(ResourceBundle $bundle): string
```

Повертає останнє повідомлення про помилку під час виклику функцій пакета.

### Список параметрів

`bundle`

Об'єкт [ResourceBundle](class.resourcebundle.html)

### Значення, що повертаються

Повертає останнє повідомлення про помилку під час виклику функцій пакета.

### Приклади

**Приклад #1 Приклад використання **resourcebundlegeterrormessage()****

```php
<?php
$r = resourcebundle_create( 'es', "/usr/share/data/myapp");
echo $r['somestring'];
if(intl_is_failure(resourcebundle_get_error_code($r))) {
    report_error("Ошибка пакета: ".resourcebundle_get_error_message($r));
}
?>
```

**Приклад #2 Приклад в об'єктно-орієнтованому стилі**

```php
<?php
$r = new ResourceBundle( 'es', "/usr/share/data/myapp");
echo $r['somestring'];
if(intl_is_failure(ResourceBundle::getErrorCode($r))) {
    report_error("Ошибка пакета: ".ResourceBundle::getErrorMessage($r));
}
?>
```

### Дивіться також

-   [resourcebundlegeterrorcode()](resourcebundle.geterrorcode.html) - Отримати останній код помилки пакета
-   [intlgeterrorcode()](function.intl-get-error-code.html) - Отримати код останньої помилки
-   [intlісfailure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою