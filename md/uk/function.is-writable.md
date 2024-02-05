---
navigation:
  - function.is-uploaded-file.md: « is\_uploaded\_file
  - function.is-writeable.md: is\_writeable »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: is\_writable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_writable

(PHP 4, PHP 5, PHP 7, PHP 8)

is\_writable — Визначає, чи є файл для запису.

### Опис

```methodsynopsis
is_writable(string $filename): bool
```

Повертає **`true`**, якщо файл `filename` існує та доступний для запису. Аргумент filename може бути ім'ям директорії, що дозволяє перевіряти директорії на доступність для запису.

Не забувайте, що PHP може звертатися до файлу від імені користувача, від якого запущений веб-сервер (зазвичай 'nobody').

### Список параметрів

`filename`

Перевіряється файл.

### Значення, що повертаються

Повертає **`true`**, якщо `filename` існує та доступний для запису.

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

### Приклади

**Пример #1 Пример использования**is\_writable()\*\*\*\*

```php
<?php
$filename = 'test.txt';
if (is_writable($filename)) {
    echo 'Файл доступен для записи';
} else {
    echo 'Файл недоступен для записи';
}
?>
```

### Примітки

> **Зауваження**: Результати цієї функції кешуються Більш детальну інформацію дивіться у розділі [clearstatcache()](function.clearstatcache.md)

**Підказка**

Починаючи з PHP 5.0.0, ця функція також може бути використана з *деякими* обгортками url. Список обгорток, що підтримуються сімейством функцій [stat()](function.stat.md), смотрите в разделе[Підтримувані протоколи та обгортки](wrappers.md)

### Дивіться також

-   [is\_readable()](function.is-readable.md) \- Визначає існування файлу і чи він доступний для читання
-   [file\_exists()](function.file-exists.md) \- Перевіряє існування вказаного файлу чи каталогу
-   [fwrite()](function.fwrite.md) \- Бінарно-безпечний запис у файл
