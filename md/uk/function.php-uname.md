---
navigation:
  - function.php-sapi-name.html: « phpsapiname
  - function.phpcredits.md: phpcredits »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: phpuname
---
# phpuname

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

phpuname — Повертає інформацію про операційну систему, на якій запущено PHP

### Опис

```methodsynopsis
php_uname(string $mode = "a"): string
```

**phpuname()** повертає опис операційної системи, де запущено PHP. Це той самий рядок, з якого починається висновок [phpinfo()](function.phpinfo.md). Для виведення назви операційної системи також можна використовувати константу **`PHP_OS`**, але майте на увазі, що ця константа містить назву операційної системи, на якій PHP було зібрано (*built*

На деяких старих UNIX-платформах отримати інформацію про поточну ОС може бути неможливим. У таких випадках функція видасть назву ОС, де PHP був зібраний. Таке трапляється, коли бібліотека, яка користується uname(), недоступна або працює некоректно.

### Список параметрів

`mode`

`mode` - одиночний символ, який визначає, яка інформація буде виводитися:

-   `'a'`: За замовчуванням. Містить усі режими у наступній послідовності `"s n r v m"`
-   `'s'`: Назва операційної системи, наприклад, `FreeBSD`
-   `'n'`: Ім'я хоста, наприклад, `localhost.example.com`
-   `'r'`: Номер релізу, наприклад, `5.1.2-RELEASE`
-   `'v'`: Інформація про версію Може сильно різнитися у різних ОС.
-   `'m'`: Архітектура процесора, наприклад, `i386`

### Значення, що повертаються

Повертає опис ОС у вигляді рядка.

### Приклади

**Приклад #1 Декілька прикладів використання **phpuname()****

```php
<?php
echo php_uname();
echo PHP_OS;

/* Разные варианты:
Linux localhost 2.4.21-0.13mdk #1 Fri Mar 14 15:08:06 EST 2003 i686
Linux

FreeBSD localhost 3.2-RELEASE #15: Mon Dec 17 08:46:02 GMT 2001
FreeBSD

Windows NT XN1 5.1 build 2600
WINNT
*/

if (strtoupper(substr(PHP_OS, 0, 3)) === 'WIN') {
    echo 'Сервер работает под управлением Windows!';
} else {
    echo 'Сервер работает под управлением ОС, отличной от Windows!';
}

?>
```

Нижче наведено декілька [Обумовлених PHP-констант](language.constants.predefined.md), які можуть виявитися корисними:

**Приклад #2 Деякі константи OS**

```php
<?php
// *nix
echo DIRECTORY_SEPARATOR; // /
echo PHP_SHLIB_SUFFIX;    // so
echo PATH_SEPARATOR;      // :

// Win*
echo DIRECTORY_SEPARATOR; // \
echo PHP_SHLIB_SUFFIX;    // dll
echo PATH_SEPARATOR;      // ;
?>
```

### Дивіться також

-   [phpversion()](function.phpversion.md) - Отримує поточну версію PHP
-   [phpsapiname()](function.php-sapi-name.html) - Повертає тип інтерфейсу між веб-сервером та PHP
-   [phpinfo()](function.phpinfo.md) - Виводить інформацію про поточну конфігурацію PHP
