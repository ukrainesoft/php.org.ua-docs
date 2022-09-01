---
navigation:
  - function.basename.html: « basename
  - function.chmod.html: chmod »
  - index.html: PHP Manual
  - ref.filesystem.html: Функції файлової системи
title: chgrp
---
# chgrp

(PHP 4, PHP 5, PHP 7, PHP 8)

chgrp — Змінює групу файлу

### Опис

```methodsynopsis
chgrp(string $filename, string|int $group): bool
```

Здійснює спробу зміни групи файлу `filename` на групу `group`

Тільки суперкористувач може довільно змінювати групу файлу; Інші користувачі можуть змінювати групу файлу лише на ті групи, членами яких є.

### Список параметрів

`filename`

Шлях до файлу.

`group`

Назва чи номер групи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Зміна групи файлів**

```php
<?php
$filename = 'shared_file.txt';
$format = "Идентификатор группы файла %s @ %s: %d\n";
printf($format, $filename, date('r'), filegroup($filename));
chgrp($filename, 8);
clearstatcache(); // сбрасываем кеш filegroup()
printf($format, $filename, date('r'), filegroup($filename));
?>
```

### Примітки

> **Зауваження**: Ця функція не застосовується для роботи з [віддаленими файлами](features.remote-files.md)оскільки файл повинен бути доступний через файлову систему сервера.

> **Зауваження**: У Windows функція мовчки завершується помилкою при застосуванні до звичайного файлу.

### Дивіться також

-   [chown()](function.chown.md) - Змінює власника файлу
-   [chmod()](function.chmod.md) - Змінює режим доступу до файлу
