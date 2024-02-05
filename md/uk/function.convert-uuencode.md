---
navigation:
  - function.convert-uudecode.md: « convert\_uudecode
  - function.count-chars.md: count\_chars »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: convert\_uuencode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# convert\_uuencode

(PHP 5, PHP 7, PHP 8)

convert\_uuencode — Кодує рядок у форматі uuencode

### Опис

```methodsynopsis
convert_uuencode(string $string): string
```

\*\*convert\_uuencode()\*\*кодирует строку с помощью алгоритма uuencode.

Кодування uuencode переводить рядки (включаючи бінарні символи) у послідовності друкованих (7-бітних) ASCII-символів, що дозволяє безпечно обмінюватися даними через мережу. Закодовані дані приблизно на 35% більше від оригіналу.

> **Зауваження** [convert\_uudecode()](function.convert-uudecode.md) не приймає ні початкової (`begin`), ні кінцевої (`end`) рядки, яка є частиною файлів (*files*) uuencoded.

### Список параметрів

`string`

Кодовані дані.

### Значення, що повертаються

Повертає закодовані дані у форматі uuencode.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | До цієї версії при спробі перетворити порожній рядок поверталося **`false`** без особливих причин. |

### Приклади

**Пример #1 Пример использования**convert\_uuencode()\*\*\*\*

```php
<?php
$some_string = "test\ntext text\r\n";

echo convert_uuencode($some_string);
?>
```

Результат виконання наведеного прикладу:

```
0=&5S=`IT97AT('1E>'0-"@``
`
```

### Дивіться також

-   [convert\_uudecode()](function.convert-uudecode.md) \- Декодує рядок із формату uuencode у звичайний вигляд
-   [base64\_encode()](function.base64-encode.md) \- Кодує дані у формат MIME base64
