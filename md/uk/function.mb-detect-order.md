---
navigation:
  - function.mb-detect-encoding.md: « mb\_detect\_encoding
  - function.mb-encode-mimeheader.md: mb\_encode\_mimeheader »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_detect\_order
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_detect\_order

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_detect\_order — Встановлює/отримує порядок визначення кодування символів

### Опис

```methodsynopsis
mb_detect_order(array|string|null $encoding = null): array|bool
```

Встановлює порядок автоматичного визначення кодування символів значення, передане в параметр `encoding`

### Список параметрів

`encoding`

Параметр`encoding` - масив (array) або розділений комами список кодувань символів. Докладніше про кодування символів, що існують в PHP, розказано в розділі «[Кодування символів, що підтримуються](mbstring.supported-encodings.md)».

Якщо параметр `encoding` не заданий або дорівнює **`null`**, функція поверне поточний порядок визначення кодувань символів як масиву.

Ця установка впливає на роботу функцій [mb\_detect\_encoding()](function.mb-detect-encoding.md) і [mb\_send\_mail()](function.mb-send-mail.md)

Модуль`mbstring` містить наступні фільтри визначення кодувань. Якщо для наступних кодувань існує неприпустима послідовність байтів, кодування завершиться невдало:

`UTF-8` `UTF-7` `ASCII` `EUC-JP`,`SJIS` `eucJP-win` `SJIS-win` `JIS` `ISO-2022-JP`

Модуль`mbstring` визначає кодування `ISO-8859-*` як `ISO-8859-*`

Определение кодировок`UTF-16` `UTF-32` `UCS2`и`UCS4` завжди буде невдалим.

### Значення, що повертаються

При установке порядка определения кодировки: возвращает\*\*`true`\*\* у разі успішного виконання або\*\*`false`\*\*в случае возникновения ошибки.

При отриманні порядку визначення кодування повертає масив кодувань у встановленому порядку.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Приклади

**Пример #1 Пример использования функции**mb\_detect\_order()\*\*\*\*

```php
<?php
/* Установка порядка определения списком перечисленных кодировок */
mb_detect_order("eucjp-win,sjis-win,UTF-8");

/* Установка порядка определения массивом */
$ary[] = "ASCII";
$ary[] = "JIS";
$ary[] = "EUC-JP";
mb_detect_order($ary);

/* Отображение текущего порядка обнаружения */
echo implode(", ", mb_detect_order());
?>
```

**Приклад #2 Приклад марних порядків визначення**

```
; Всегда определяет как ISO-8859-1
detect_order = ISO-8859-1, UTF-8

; Всегда определяет как UTF-8, так как ASCII/UTF-7 —
; подмножество UTF-8
detect_order = UTF-8, ASCII, UTF-7
```

### Дивіться також

-   [mb\_internal\_encoding()](function.mb-internal-encoding.md) \- Встановлює/отримує внутрішнє кодування скрипту
-   [mb\_http\_input()](function.mb-http-input.md) \- Визначає кодування символів вхідних даних HTTP-запиту
-   [mb\_http\_output()](function.mb-http-output.md) \- Встановлює/отримує кодування символів виводу HTTP
-   [mb\_send\_mail()](function.mb-send-mail.md) \- Надсилає закодований електронний лист
