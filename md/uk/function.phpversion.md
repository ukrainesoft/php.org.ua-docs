Отримує поточну версію PHP

-   [« phpinfo](function.phpinfo.html)
    
-   [putenv »](function.putenv.html)
    
-   [PHP Manual](index.html)
    
-   [Опції PHP/інформаційні функції](ref.info.html)
    
-   Отримує поточну версію PHP
    

# phpversion

(PHP 4, PHP 5, PHP 7, PHP 8)

phpversion — Отримує поточну версію PHP

### Опис

```methodsynopsis
phpversion(?string $extension = null): string|false
```

Повертає рядок з номером версії PHP-інтерпретатора або модуля.

### Список параметрів

`extension`

Необов'язкове ім'я модуля.

### Значення, що повертаються

Повертає поточну версію PHP у вигляді рядка (string). Якщо у параметрі `extension` вказано строкове значення (string), **phpversion()** поверне версію цього модуля або **`false`**, якщо немає інформації про версію або модуль не ввімкнено.

### список змін

| Версия | Описание                                  |
|--------|-------------------------------------------|
|        | `extension` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **phpversion()****

```php
<?php
// Выводит строку типа 'Текущая версия PHP: 4.1.1'
echo 'Текущая версия PHP: ' . phpversion();

// Выводит строку типа '2.0' или ничего, если модуль не включён
echo phpversion('tidy');
?>
```

**Приклад #2 Приклад використання **`PHP_VERSION_ID`****

```php
<?php
// PHP_VERSION_ID доступна в версиях PHP 5.2.7 и выше. Если
// наша версия ниже, можно её сэмулировать
if (!defined('PHP_VERSION_ID')) {
    $version = explode('.', PHP_VERSION);

    define('PHP_VERSION_ID', ($version[0] * 10000 + $version[1] * 100 + $version[2]));
}

// PHP_VERSION_ID определена как число. Чем больше число, тем новее
// PHP. Эта константа задаётся по той же схеме, что приведена выше:
//
// $version_id = $major_version * 10000 + $minor_version * 100 + $release_version;
//
// Теперь с PHP_VERSION_ID можно проверять, какая функциональность есть в
// текущей версии PHP. Не обязательно пользоваться version_compare()
// каждый раз, когда требуется проверить, поддерживает ли PHP нужную
// нам функцию.
//
// Например, мы можем задать значения констант PHP_VERSION_*,
// которые недоступны в версиях ранее 5.2.7

if (PHP_VERSION_ID < 50207) {
    define('PHP_MAJOR_VERSION',   $version[0]);
    define('PHP_MINOR_VERSION',   $version[1]);
    define('PHP_RELEASE_VERSION', $version[2]);

    // и так далее ...
}
?>
```

### Примітки

> **Зауваження**
> 
> Ця інформація також доступна через певну константу **`PHP_VERSION`**. Більш детальну інформацію можна отримати за допомогою констант **`PHP_VERSION_*`**

### Дивіться також

-   [Константи PHPVERSION](reserved.constants.html#reserved.constants.core)
-   [versioncompare()](function.version-compare.html) - Порівнює два "стандартизовані" рядки з номером версії PHP
-   [phpinfo()](function.phpinfo.html) - Виводить інформацію про поточну конфігурацію PHP
-   [phpcredits()](function.phpcredits.html) - Виводить список розробників PHP
-   [zendversion()](function.zend-version.html) - Отримує версію двигуна Zend