Очищує кеш стану файлів

-   [« chown](function.chown.html)
    
-   [copy »](function.copy.html)
    
-   [PHP Manual](index.html)
    
-   [Функции файловой системы](ref.filesystem.html)
    
-   Очищує кеш стану файлів
    

# clearstatcache

(PHP 4, PHP 5, PHP 7, PHP 8)

clearstatcache — Очищає кеш стану файлів

### Опис

```methodsynopsis
clearstatcache(bool $clear_realpath_cache = false, string $filename = ""): void
```

Для забезпечення більшої продуктивності під час використання функцій [stat()](function.stat.html) [lstat()](function.lstat.html) або будь-якої іншої функції, перерахованих у наведеному нижче списку, PHP кешує результати виконання. Однак, у деяких випадках вам може знадобитися очищення цього кешу. Наприклад, коли ваш скрипт кілька разів перевіряє стан того самого файлу, який може бути змінений або видалений під час виконання скрипту, ви можете захотіти очистити кеш стану. У цьому випадку необхідно використати функцію **clearstatcache()** для очищення в PHP кешованої інформації про вказаний файл.

Зверніть увагу, що PHP не кешує інформацію про неіснуючі файли. Так що якщо ви викличете [file\_exists()](function.file-exists.html) на неіснуючому файлі, вона повертатиме **`false`** поки ви не створите цей файл. Якщо ж ви створите файл, вона повертатиме **`true`**, навіть якщо ви його видалите. Однак, функція [unlink()](function.unlink.html) очистити дані кеш автоматично.

> **Зауваження**
> 
> Ця функція кешує інформацію про певні файли, тому має сенс викликати **clearstatcache()** тільки в тому випадку, якщо ви робите кілька операцій з одним і тим же файлом і не хочете отримувати кешовану інформацію про цей файл.

Список функцій, результати виконання яких кешуються: [stat()](function.stat.html) [lstat()](function.lstat.html) [file\_exists()](function.file-exists.html) [is\_writable()](function.is-writable.html) [is\_readable()](function.is-readable.html) [is\_executable()](function.is-executable.html) [is\_file()](function.is-file.html) [is\_dir()](function.is-dir.html) [is\_link()](function.is-link.html) [filectime()](function.filectime.html) [fileatime()](function.fileatime.html) [filemtime()](function.filemtime.html) [fileinode()](function.fileinode.html) [filegroup()](function.filegroup.html) [fileowner()](function.fileowner.html) [filesize()](function.filesize.html) [filetype()](function.filetype.html) і [fileperms()](function.fileperms.html)

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
$file = 'output_log.txt';

function get_owner($file)
{
    $stat = stat($file);
    $user = posix_getpwuid($stat['uid']);
    return $user['name'];
}

$format = "UID @ %s: %s\n";

printf($format, date('r'), get_owner($file));

chown($file, 'ross');
printf($format, date('r'), get_owner($file));

clearstatcache();
printf($format, date('r'), get_owner($file));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
UID @ Sun, 12 Oct 2008 20:48:28 +0100: root
UID @ Sun, 12 Oct 2008 20:48:28 +0100: root
UID @ Sun, 12 Oct 2008 20:48:28 +0100: ross
```