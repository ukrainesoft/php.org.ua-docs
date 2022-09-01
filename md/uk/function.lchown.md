---
navigation:
  - function.lchgrp.md: « lchgrp
  - function.link.md: link »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: lchown
---
# lchown

(PHP 5> = 5.1.3, PHP 7, PHP 8)

lchown — Змінює власника символічного посилання

### Опис

```methodsynopsis
lchown(string $filename, string|int $user): bool
```

Намагається змінити власника символічного посилання `filename` на зазначеного в `user` користувача.

Тільки суперкористувач може змінювати власника символічного посилання.

### Список параметрів

`filename`

Шлях до файлу.

`user`

Ім'я користувача чи номер.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Зміна власника символічного посилання**

```php
<?php
$target = 'output.php';
$link = 'output.html';
symlink($target, $link);

lchown($link, 8);
?>
```

### Примітки

> **Зауваження**: Ця функція не застосовується для роботи з [віддаленими файлами](features.remote-files.html)оскільки файл повинен бути доступний через файлову систему сервера.

> **Зауваження**: Для Windows-платформ ця функція не реалізована.

### Дивіться також

-   [chown()](function.chown.md) - Змінює власника файлу
-   [lchgrp()](function.lchgrp.md) - Змінює групу, якій належить символічне посилання
-   [chgrp()](function.chgrp.md) - Змінює групу файлу
-   [chmod()](function.chmod.md) - Змінює режим доступу до файлу
