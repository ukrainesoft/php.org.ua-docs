---
navigation:
  - mysqli.debug.md: '« mysqli::debug'
  - mysqli.errno.md: 'mysqli::$errno »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::dump\_debug\_info'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::dump\_debug\_info

# mysqli\_dump\_debug\_info

(PHP 5, PHP 7, PHP 8)

mysqli::dump\_debug\_info -- mysqli\_dump\_debug\_info — Журналування налагоджувальної інформації

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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [mysqli\_debug()](mysqli.debug.md) \- Виконує процедури налагодження
