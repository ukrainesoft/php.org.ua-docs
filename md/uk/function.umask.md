---
navigation:
  - function.touch.md: « touch
  - function.unlink.md: unlink »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: umask
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# umask

(PHP 4, PHP 5, PHP 7, PHP 8)

umask — Змінює поточну маску прав доступу для новостворених файлів та каталогів (umask)

### Опис

```methodsynopsis
umask(?int $mask = null): int
```

Функция\*\*umask()\*\*устанавливает применяемую PHP по умолчанию umask в значение параметра`mask` & 0777 та повертає стару umask. Якщо PHP працює як серверний модуль, umask відновлюватиметься після закінчення кожного запиту.

### Список параметрів

`mask`

Новий umask.

### Значення, що повертаються

Якщо параметр `mask`равен\*\*`null`**, функция**umask()\*\* просто повертає поточну umask, інакше повертається стара umask.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`mask` тепер може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад використання функції** umask()\*\*\*\*

```php
<?php
$old = umask(0);
chmod("/path/some_dir/some_file.txt", 0755);
umask($old);

// Проверка
if ($old != umask()) {
    die('При восстановлении umask произошла ошибка');
}
?>
```

### Примітки

> **Зауваження** :
> 
> Уникайте виклику цієї функції на багатопотокових веб-серверах. Найкраще змінити права створеного файлу функцією [chmod()](function.chmod.md)Функция**umask()** може викликати несподівану поведінку одночасно скриптів і самого веб-сервера, оскільки вони всі будуть використовувати одну і ту ж umask.
