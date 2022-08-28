Запускає команду через командну оболонку Bourne та відкриває для процесу потік PTY

-   [« expect\_expectl](function.expect-expectl.html)
    
-   [PCNTL »](book.pcntl.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Expect](ref.expect.html)
    
-   Запускає команду через командну оболонку Bourne та відкриває для процесу потік PTY
    

# expectpopen

(PECL expect >= 0.1.0)

expectpopen — Запускає команду через командну оболонку Bourne та відкриває для процесу потік PTY

### Опис

```methodsynopsis
expect_popen(string $command): resource
```

Запускає команду через командну оболонку Bourne та відкриває для процесу потік PTY.

### Список параметрів

`command`

Команда для запуску.

### Значення, що повертаються

Повертає потік PTY для `stdio` `stdout`, і `stderr` процесу.

У разі виникнення помилки повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **expectpopen()****

```php
<?php
// Соединение с CVS репозиторием PHP.net:
$stream = expect_popen ("cvs -d :pserver:anonymous@cvs.php.net:/repository login");
sleep (3);
fwrite ($stream, "phpfi\n");
fclose ($stream);
?>
```

### Дивіться також

-   [popen()](function.popen.html) - Відкриває файловий покажчик процесу