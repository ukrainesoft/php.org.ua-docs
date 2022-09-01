---
navigation:
  - function.gzgetc.md: « gzgetc
  - function.gzgetss.md: gzgetss »
  - index.md: PHP Manual
  - ref.zlib.md: Функции Zlib
title: gzgets
---
# gzgets

(PHP 4, PHP 5, PHP 7, PHP 8)

gzgets — Отримати рядок із покажчика файлу

### Опис

```methodsynopsis
gzgets(resource $stream, ?int $length = null): string|false
```

Отримує рядок (несжатий) з gz-файлу, його довжина обмежується `length` - 1 байт. Читання закінчується при досягненні максимальної довжини, кінця рядка або кінця файлу (EOF), залежно від того, що настане раніше.

### Список параметрів

`stream`

Вказівник на файл gz. Він має бути коректним і повинен вказувати на файл, успішно відкритий. [gzopen()](function.gzopen.md)

`length`

Максимальний розмір даних, що повертаються.

### Значення, що повертаються

Розпакований рядок або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `length` тепер припускає значення null; раніше значення за умовчанням було `1024` |

### Приклади

**Приклад #1 Приклад використання **gzgets()****

```php
<?php
$handle = gzopen('somefile.gz', 'r');
while (!gzeof($handle)) {
   $buffer = gzgets($handle, 4096);
   echo $buffer;
}
gzclose($handle);
?>
```

### Дивіться також

-   [gzopen()](function.gzopen.md) - Відкрити gz-файл
-   [gzgetc()](function.gzgetc.md) - Отримати символ із покажчика на gz-файл
-   [gzwrite()](function.gzwrite.md) - Бінарний запис у gz-файл
