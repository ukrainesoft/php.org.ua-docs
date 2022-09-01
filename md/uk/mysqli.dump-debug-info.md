---
navigation:
  - mysqli.debug.md: '« mysqli::debug'
  - mysqli.errno.md: 'mysqli::$errno »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::dumpdebuginfo'
---
# mysqli::dumpdebuginfo

# mysqlidumpdebuginfo

(PHP 5, PHP 7, PHP 8)

mysqli::dumpdebuginfo -- mysqlidumpdebuginfo — Журналування налагоджувальної інформації

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::dump_debug_info(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_dump_debug_info(mysqli $mysql): bool
```

Функція розроблена для запуску від імені користувача з привілеями SUPER і використовується для складання налагоджувальної інформації в журнал сервера MySQL, до якого здійснено підключення.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqlidebug()](mysqli.debug.md) - Виконує процедури налагодження
