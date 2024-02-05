---
navigation:
  - function.expect-expectl.md: « expect\_expectl
  - book.pcntl.md: PCNTL »
  - index.md: PHP Manual
  - ref.expect.md: Опції Expect
title: expect\_popen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# expect\_popen

(PECL expect >= 0.1.0)

expect\_popen — Запускає команду через командну оболонку Bourne та відкриває для процесу потік PTY

### Опис

```methodsynopsis
expect_popen(string $command): resource
```

Запускає команду через командну оболонку Bourne та відкриває для процесу потік PTY.

### Список параметрів

`command`

Команда для запуску.

### Значення, що повертаються

Повертає потік PTY для `stdio` `stdout`, и`stderr`процесса.

У разі виникнення помилки повертає **`false`**

### Приклади

**Пример #1 Пример использования**expect\_popen()\*\*\*\*

```php
<?php
// Соединение с CVS репозиторием PHP.net:
$stream = expect_popen ("cvs -d :pserver:anonymous@cvs.php.net:/repository login");
sleep (3);
fwrite ($stream, "phpfi\n");
fclose ($stream);
?>
```

### Дивіться також

-   [popen()](function.popen.md) \- Відкриває файловий покажчик процесу
