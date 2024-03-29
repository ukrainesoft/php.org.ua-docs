---
navigation:
  - function.phpinfo.md: « phpinfo
  - function.putenv.md: putenv »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: phpversion
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Повертає поточну версію PHP у вигляді рядка (string). Якщо у параметрі `extension`указано строковое значение (string),**phpversion()** поверне версію цього модуля або **`false`**, якщо немає інформації про версію або модуль не ввімкнено.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `extension` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** phpversion()\*\*\*\*

```php
<?php
// Выводит строку типа 'Текущая версия PHP: 4.1.1'
echo 'Текущая версия PHP: ' . phpversion();

// Выводит строку типа '2.0' или ничего, если модуль не включён
echo phpversion('tidy');
?>
```

**Приклад #2 Приклад використання** `PHP_VERSION_ID`\*\*\*\*

```php
<?php
// PHP_VERSION_ID доступна в версиях PHP 5.2.7 и выше. Если
// наша версия ниже, можно её сэмулировать
if (!defined('PHP_VERSION_ID')) {
    $version = explode('.', PHP_VERSION);

    define('PHP_VERSION_ID', ($version[0] * 10000 + $version[1] * 100 + $version[2]));
}

// PHP_VERSION_ID определена как число. Чем больше число, тем новее
// PHP. Эта константа задаётся по той же схеме, что приведена выше:
//
// $version_id = $major_version * 10000 + $minor_version * 100 + $release_version;
//
// Теперь с PHP_VERSION_ID можно проверять, какая функциональность есть в
// текущей версии PHP. Не обязательно пользоваться version_compare()
// каждый раз, когда требуется проверить, поддерживает ли PHP нужную
// нам функцию.
//
// НаПриклад, мы можем задать значения констант PHP_VERSION_*,
// которые недоступны в версиях ранее 5.2.7

if (PHP_VERSION_ID < 50207) {
    define('PHP_MAJOR_VERSION',   $version[0]);
    define('PHP_MINOR_VERSION',   $version[1]);
    define('PHP_RELEASE_VERSION', $version[2]);

    // и так далее ...
}
?>
```

### Примітки

> **Зауваження** :
> 
> Ця інформація також доступна через певну константу **`PHP_VERSION`**. Більш детальну інформацію можна отримати за допомогою констант **`PHP_VERSION_*`**

> **Зауваження** :
> 
> Деякі модулі можуть визначати власний номер версії. Однак більшість модулів, що входять до комплекту поставки, як номер версії використовують версію PHP.

### Дивіться також

-   [Константи PHP\_VERSION](reserved.constants.md#reserved.constants.core)
-   [version\_compare()](function.version-compare.md) \- Порівнює два «стандартизовані» рядки з номером версії PHP
-   [phpinfo()](function.phpinfo.md) \- Виводить інформацію про поточну конфігурацію PHP
-   [phpcredits()](function.phpcredits.md) \- Виводить список розробників PHP
-   [zend\_version()](function.zend-version.md) \- Отримує версію двигуна Zend
