---
navigation:
  - function.glob.md: « glob
  - function.is-executable.md: is\_executable »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: is\_dir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_dir

(PHP 4, PHP 5, PHP 7, PHP 8)

is\_dir — Визначає, чи ім'я файлу є директорією.

### Опис

```methodsynopsis
is_dir(string $filename): bool
```

Визначає, чи ім'я файлу є директорією.

### Список параметрів

`filename`

Шлях до файлу. Якщо `filename` є відносним ім'ям, він перевірятиметься щодо поточної робочої директорії. Якщо `filename` є символічним або жорстким посиланням, то посилання буде розкрито та перевірено. При включеному [open\_basedir](ini.core.md#ini.open-basedir) можуть застосовуватись подальші обмеження.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо файл існує і є директорією, інакше повертається **`false`**

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад використання функції** is\_dir()\*\*\*\*

```php
<?php
var_dump(is_dir('a_file.txt'));
var_dump(is_dir('bogus_dir/abc'));

var_dump(is_dir('..')); // на одну директорию выше
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(false)
bool(true)
```

### Примітки

> **Зауваження**: Результати цієї функції кешуються Більш детальну інформацію дивіться у розділі [clearstatcache()](function.clearstatcache.md)

**Підказка**

Починаючи з PHP 5.0.0, ця функція також може бути використана з *деякими* обгортками url. Список обгорток, що підтримуються сімейством функцій [stat()](function.stat.md), смотрите в разделе[Підтримувані протоколи та обгортки](wrappers.md)

### Дивіться також

-   [chdir()](function.chdir.md) \- Змінює каталог
-   [dir()](function.dir.md) \- Повертає екземпляр класу Directory
-   [opendir()](function.opendir.md) \- Відкриває дескриптор каталогу
-   [is\_file()](function.is-file.md) \- Визначає, чи файл є звичайним файлом
-   [is\_link()](function.is-link.md) \- Визначає, чи є файл символічним посиланням
