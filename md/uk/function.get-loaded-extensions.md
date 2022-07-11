- [«get_included_files](function.get-included-files.md)
- [get_magic_quotes_gpc »](function.get-magic-quotes-gpc.md)

- [PHP Manual](index.md)
- [Опції PHP/інформаційні функції](ref.info.md)
- Повертає масив імен усіх скомпілованих та завантажених модулів

#get_loaded_extensions

(PHP 4, PHP 5, PHP 7, PHP 8)

get_loaded_extensions — Повертає масив імен усіх скомпільованих та
завантажених модулів

### Опис

**get_loaded_extensions**(bool `$zend_extensions` = **`false`**): array

Функція повертає масив імен всіх скомпілованих та завантажених у
інтерпретатор PHP модулів.

### Список параметрів

`zend_extensions`
Повертати лише модулі Zend або звичайні модулі, такі як mysqli. за
замовчуванням **`false`** (повернення звичайних модулів).

### Значення, що повертаються

Повертає індексований масив назв усіх модулів.

### Приклади

**Приклад #1 Приклад використання **get_loaded_extensions()****

` <?phpprint_r(get_loaded_extensions());?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => xml
[1] => wddx
[2] => standard
[3] => session
[4] => posix
[5] => pgsql
[6] => pcre
[7] => gd
[8] => ftp
[9] => db
[10] => calendar
[11] => bcmath
)

### Дивіться також

- [get_extension_funcs()](function.get-extension-funcs.md) -
Повертає масив імен функцій модуля
- [extension_loaded()](function.extension-loaded.md) - Визначає,
чи завантажений модуль
- [dl()](function.dl.md) - Завантажує модуль PHP під час виконання
- [phpinfo()](function.phpinfo.md) - Виводить інформацію про поточну
конфігурації PHP
