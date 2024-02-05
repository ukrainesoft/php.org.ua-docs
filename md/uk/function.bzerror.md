---
navigation:
  - function.bzerrno.md: « bzerrno
  - function.bzerrstr.md: bzerrstr »
  - index.md: PHP Manual
  - ref.bzip2.md: Функції Bzip2
title: bzerror
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bzerror

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

bzerror — Повертає код та рядок помилки роботи з bzip2 у вигляді масиву

### Опис

```methodsynopsis
bzerror(resource $bz): array
```

Повертає асоціативний масив із кодом та рядком помилки, що сталася з переданим файловим покажчиком.

### Список параметрів

`bz`

Файловий покажчик. Має бути коректним і вказувати на файл, успішно відкритий [bzopen()](function.bzopen.md)

### Значення, що повертаються

Повертає асоціативний масив із кодом помилки з ключем `errno`, і рядком помилки з ключем `errstr`

### Приклади

**Приклад #1 Приклад використання** bzerror()\*\*\*\*

```php
<?php
$error = bzerror($bz);

echo $error["errno"];
echo $error["errstr"];
?>
```

### Дивіться також

-   [bzerrno()](function.bzerrno.md) \- Повертає код помилки роботи з bzip2
-   [bzerrstr()](function.bzerrstr.md) \- Повертає рядок помилки роботи з bzip2
