---
navigation:
  - function.mb-detect-encoding.md: « mbdetectencoding
  - function.mb-encode-mimeheader.md: мбencodemimeheader »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбdetectorder
---
# мбdetectorder

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбdetectorder — Встановлення/отримання списку кодувань для механізмів визначення кодування

### Опис

```methodsynopsis
mb_detect_order(array|string|null $encoding = null): array|bool
```

У `encoding` задається порядок, у якому механізми автоматичного визначення кодувань їх перевірятимуть.

### Список параметрів

`encoding`

`encoding` - масив (array) або рядок, в якому перераховані кодування через кому. Дивіться [Підтримувані кодування](mbstring.supported-encodings.md)

Якщо `encoding` опущено, функція поверне поточний список кодувань як масиву.

Ця установка впливає на роботу функцій [мбdetectencoding()](function.mb-detect-encoding.md) і [мбsendmail()](function.mb-send-mail.md)

У `mbstring` на даний момент реалізовані такі фільтри для визначення кодувань. Якщо послідовність байт у вихідному рядку не відповідатиме жодному з перерахованих кодувань, визначення кодування завершиться невдачею.

`UTF-8` `UTF-7` `ASCII` `EUC-JP``SJIS` `eucJP-win` `SJIS-win` `JIS` `ISO-2022-JP`

Кодування `ISO-8859-*` `mbstring` завжди визначає як `ISO-8859-*`

Для кодувань `UTF-16` `UTF-32` `UCS2` і `UCS4` автоматичне визначення завжди завершуватиметься невдачею.

### Значення, що повертаються

При установці порядку визначення кодування, залежно від успішності, повертає **`true`** або **`false`**

При отриманні порядку визначення кодування повертається відсортований масив кодувань.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер параметр `encoding` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад використання **мбdetectorder()****

```php
<?php
/* Установка порядка определения в виде упорядоченного списка */
mb_detect_order("eucjp-win,sjis-win,UTF-8");

/* Установка списка кодировок в виде Масива */
$ary[] = "ASCII";
$ary[] = "JIS";
$ary[] = "EUC-JP";
mb_detect_order($ary);

/* Вывод текущего списка кодировок */
echo implode(", ", mb_detect_order());
?>
```

**Приклад #2 Приклад марного порядку визначення**

```
; Всегда определяет как ISO-8859-1
detect_order = ISO-8859-1, UTF-8

; Всегда определяет как UTF-8, так как ASCII/UTF-7
; являются подмножеством UTF-8
detect_order = UTF-8, ASCII, UTF-7
```

### Дивіться також

-   [мбinternalencoding()](function.mb-internal-encoding.md) - Встановлення/отримання внутрішнього кодування скрипту
-   [мбhttpinput()](function.mb-http-input.md) - Визначення кодування символів вхідних даних HTTP-запиту
-   [мбhttpoutput()](function.mb-http-output.md) - Встановлення/отримання кодування символів виводу HTTP
-   [мбsendmail()](function.mb-send-mail.md) - Надсилання закодованого повідомлення
