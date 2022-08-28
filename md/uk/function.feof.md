Перевіряє, чи кінець файлу досягнуто.

-   [« fdatasync](function.fdatasync.html)
    
-   [fflush »](function.fflush.html)
    
-   [PHP Manual](index.html)
    
-   [Функции файловой системы](ref.filesystem.html)
    
-   Перевіряє, чи кінець файлу досягнуто.
    

# feof

(PHP 4, PHP 5, PHP 7, PHP 8)

feof — Перевіряє, чи кінець файлу досягнуто.

### Опис

```methodsynopsis
feof(resource $stream): bool
```

Перевіряє, чи кінець файлу досягнуто.

### Список параметрів

`stream`

Вказівник на файл повинен бути коректним і вказувати на файл, успішно відкритий функціями [fopen()](function.fopen.html) або [fsockopen()](function.fsockopen.html) (і все ще не закритий функцією [fclose()](function.fclose.html)

### Значення, що повертаються

Повертає **`true`**якщо вказівник файлу вказує на EOF або сталася помилка (у тому числі перевищено час очікування сокету), інакше повертає **`false`**

### Примітки

**Увага**

Якщо підключення відкрите за допомогою [fsockopen()](function.fsockopen.html), не було закрито сервером, **feof()** повисне. Для варіанта обходу цієї поведінки дивіться такий приклад:

**Приклад #1 Обробка часу очікування з функцією **feof()****

```php
<?php
function safe_feof($fp, &$start = NULL) {
 $start = microtime(true);

 return feof($fp);
}

/* Предположим, что $fp был ранее открыт с помощью fsockopen() */

$start = NULL;
$timeout = ini_get('default_socket_timeout');

while(!safe_feof($fp, $start) && (microtime(true) - $start) < $timeout)
{
 /* Обработка */
}
?>
```

**Увага**

Якщо передано неправильний файловий покажчик, то ви можете отримати нескінченний цикл, оскільки **feof()** не зможе повернути **`true`**

**Приклад #2 Приклад **feof()** з невірним файловим покажчиком**

```php
<?php
// если файл не может быть прочтён или не существует, fopen вернёт FALSE
$file = @fopen("no_such_file", "r");

// FALSE от fopen вызовет предупреждение и следующий цикл станет бесконечным
while (!feof($file)) {
}

fclose($file);
?>
```