---
navigation:
  - function.posix-ttyname.md: « posix\_ttyname
  - book.exec.md: Запуск програми "
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_uname
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_uname

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_uname — Повертає інформацію про систему

### Опис

```methodsynopsis
posix_uname(): array|false
```

Повертає інформацію про систему.

Posix вимагає, щоб розробники не покладалися на певний формат різних значень, наприклад, припущення, що номер релізу має складатися з трьох чисел. Теж стосується й іншої інформації, що повертається цією функцією.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив з інформацією про систему, включаючи такі елементи:

-   sysname – назва операційної системи (наприклад Linux)
-   nodename – системне ім'я (наприклад valiant)
-   release – номер релізу (наприклад 2.2.10)
-   version - версія операційної системи (наприклад #4 Tue Jul 20 17:01:36 MEST 1999)
-   machine – архітектура системи (наприклад i586)
-   domainname - DNS ім'я домену (наприклад, example.com)

domainname це розширення GNU, а не частина POSIX.1, тому це поле доступне тільки для GNU систем або при використанні бібліотеки GNU libc.

Функція повертає \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** posix\_uname()\*\*\*\*

```php
<?php
$uname=posix_uname();
print_r($uname);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [sysname] => Linux
    [nodename] => funbox
    [release] => 2.6.20-15-server
    [version] => #2 SMP Sun Apr 15 07:41:34 UTC 2007
    [machine] => i686
)
```
