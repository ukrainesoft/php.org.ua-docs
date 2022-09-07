---
navigation:
  - function.chown.md: « chown
  - function.copy.md: copy »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: clearstatcache
---
# clearstatcache

(PHP 4, PHP 5, PHP 7, PHP 8)

clearstatcache — Очищає кеш стану файлів

### Опис

```methodsynopsis
clearstatcache(bool $clear_realpath_cache = false, string $filename = ""): void
```

Для забезпечення більшої продуктивності під час використання функцій [stat()](function.stat.md) [lstat()](function.lstat.md) або будь-якої іншої функції, перерахованих у наведеному нижче списку, PHP кешує результати виконання. Однак, у деяких випадках вам може знадобитися очищення цього кешу. Наприклад, коли ваш скрипт кілька разів перевіряє стан того самого файлу, який може бути змінений або видалений під час виконання скрипту, ви можете захотіти очистити кеш стану. У цьому випадку необхідно використати функцію **clearstatcache()** для очищення в PHP кешованої інформації про вказаний файл.

Зверніть увагу, що PHP не кешує інформацію про неіснуючі файли. Так що якщо ви викличете [fileexists()](function.file-exists.md) на неіснуючому файлі, вона повертатиме **`false`** поки ви не створите цей файл. Якщо ж ви створите файл, вона повертатиме **`true`**, навіть якщо ви його видалите. Однак, функція [unlink()](function.unlink.md) очистити дані кеш автоматично.

> **Зауваження**
> 
> Ця функція кешує інформацію про певні файли, тому має сенс викликати **clearstatcache()** тільки в тому випадку, якщо ви робите кілька операцій з одним і тим же файлом і не хочете отримувати кешовану інформацію про цей файл.

Список функцій, результати виконання яких кешуються: [stat()](function.stat.md) [lstat()](function.lstat.md) [fileexists()](function.file-exists.md) [ісwritable()](function.is-writable.md) [ісreadable()](function.is-readable.md) [ісexecutable()](function.is-executable.md) [ісfile()](function.is-file.md) [ісdir()](function.is-dir.md) [ісlink()](function.is-link.md) [filectime()](function.filectime.md) [fileatime()](function.fileatime.md) [filemtime()](function.filemtime.md) [fileinode()](function.fileinode.md) [filegroup()](function.filegroup.md) [fileowner()](function.fileowner.md) [filesize()](function.filesize.md) [filetype()](function.filetype.md) і [fileperms()](function.fileperms.md)

### Список параметрів

`clear_realpath_cache`

Чи потрібно *також* очищати кеш realpath.

`filename`

Очистити кеш realpath тільки для певного імені файлу; використовується тільки в тому випадку, якщо параметр `clear_realpath_cache` встановлено значення **`true`**

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **clearstatcache()****

```php
<?php
$file = 'output_log.txt';

function get_owner($file)
{
    $stat = stat($file);
    $user = posix_getpwuid($stat['uid']);
    return $user['name'];
}

$format = "UID @ %s: %s\n";

printf($format, date('r'), get_owner($file));

chown($file, 'ross');
printf($format, date('r'), get_owner($file));

clearstatcache();
printf($format, date('r'), get_owner($file));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
UID @ Sun, 12 Oct 2008 20:48:28 +0100: root
UID @ Sun, 12 Oct 2008 20:48:28 +0100: root
UID @ Sun, 12 Oct 2008 20:48:28 +0100: ross
```
