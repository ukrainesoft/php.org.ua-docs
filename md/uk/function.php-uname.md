- [«php_sapi_name](function.php-sapi-name.md)
- [phpcredits]](function.phpcredits.md)

- [PHP Manual](index.md)
- [Опції PHP/інформаційні функції](ref.info.md)
- Повертає інформацію про операційну систему, на якій запущено
PHP

# php_uname

(PHP 4 \>= 4.0.2, PHP 5, PHP 7, PHP 8)

php_uname — Повертає інформацію про операційну систему, на якій
запущений PHP

### Опис

**php_uname**(string `$mode` = "a"): string

**php_uname()** повертає опис операційної системи, на якій
запущено PHP. Це той самий рядок, з якого починається виведення
[phpinfo()](function.phpinfo.md). Для виведення назви операційної
системи також можна використовувати константу **`PHP_OS`**, але майте на увазі
виду, що ця константа містить назву операційної системи,
якою PHP був зібраний (*built*).

На деяких старих UNIX-платформах отримати інформацію про поточну ОС
може бути неможливим. У таких випадках функція видасть назву ОС,
на якій PHP було зібрано. Таке трапляється, коли бібліотека, якою
користується uname(), недоступною або працює некоректно.

### Список параметрів

`mode`
`mode` - одиночний символ, який визначає, яка інформація буде
виводитися:

- ``a'`: За замовчуванням. Містить всі режими в наступному
послідовності "s n r v m".
- ``s'`: Назва операційної системи, наприклад, `FreeBSD`.
- ``n'`: Ім'я хоста, наприклад, `localhost.example.com`.
- ``r'`: Номер релізу, наприклад, `5.1.2-RELEASE`.
- ``v'`: Інформація про версію. Може сильно різнитися у різних ОС.
- ``m'`: Архітектура процесора, наприклад, `i386`.

### Значення, що повертаються

Повертає опис ОС у вигляді рядка.

### Приклади

**Приклад #1 Кілька прикладів використання **php_uname()****

`<?phpecho php_uname();echo PHP_OS;/* Різні варіанти:Linux localhost 2.4.21-0.13mdk #1 Fri Mar 14 15:08:06 EST 2003 i8          :02 GMT 2001FreeBSDWindows NT XN1 5.1 build 2600WINNT*/if (strtoupper(substr(PHP_OS, 0, 3)) === 'WIN') {    echo 'Сервер работает под управлением Windows!';} else {    echo 'Сервер работает под управлінням ОС, відмінної від Windows!';}?> `

Нижче наведено декілька [Предвизначених PHP-констант](language.constants.predefined.md), які можуть бути
виявитися корисними:

**Приклад #2 Деякі константи OS**

`<?php//**nixecho DIRECTORY_SEPARATOR; // /echo PHP_SHLIB_SUFFIX; // soecho PATH_SEPARATOR; // :// Win*echo DIRECTORY_SEPARATOR; // cho  PHP_SHLIB_SUFFIX; // dllecho PATH_SEPARATOR; // ;?> `

### Дивіться також

- [phpversion()](function.phpversion.md) - Отримує поточну версію
PHP
- [php_sapi_name()](function.php-sapi-name.md) - Повертає тип
інтерфейсу між веб-сервером і PHP
- [phpinfo()](function.phpinfo.md) - Виводить інформацію про поточну
конфігурації PHP
