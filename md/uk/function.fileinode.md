---
navigation:
  - function.filegroup.html: « filegroup
  - function.filemtime.html: filemtime »
  - index.html: PHP Manual
  - ref.filesystem.html: Функції файлової системи
title: fileinode
---
# fileinode

(PHP 4, PHP 5, PHP 7, PHP 8)

fileinode — Повертає індексний дескриптор файлу

### Опис

```methodsynopsis
fileinode(string $filename): int|false
```

Повертає індексний дескриптор файлу.

### Список параметрів

`filename`

Шлях до файлу.

### Значення, що повертаються

Повертає номер індексного дескриптора файлу або **`false`** у разі виникнення помилки.

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Порівняння індексного дескриптора файлу з поточним файлом**

```php
<?php
$filename = 'index.php';
if (getmyinode() == fileinode($filename)) {
    echo 'Вы проверяете текущий файл.';
}
?>
```

### Примітки

> **Зауваження**: Результати цієї функції кешуються Більш детальну інформацію дивіться у розділі [clearstatcache()](function.clearstatcache.html)

**Підказка**

Починаючи з PHP 5.0.0, ця функція також може бути використана з *деякими* обгортками url. Список обгорток, що підтримуються сімейством функцій [stat()](function.stat.html), дивіться у розділі [Підтримувані протоколи та обгортки](wrappers.html)

### Дивіться також

-   [getmyinode()](function.getmyinode.html) - Отримує значення inode поточного скрипту
-   [stat()](function.stat.html) - Повертає інформацію про файл
