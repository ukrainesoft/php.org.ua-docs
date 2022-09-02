---
navigation:
  - function.mb-convert-case.md: « mbconvertcase
  - function.mb-convert-kana.md: мбconvertkana »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбconvertencoding
---
# мбconvertencoding

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбconvertencoding — Перетворює рядок з одного кодування символів на інший

### Опис

```methodsynopsis
mb_convert_encoding(array|string $string, string $to_encoding, array|string|null $from_encoding = null): array|string|false
```

Перетворює параметр `string` з кодування `to_encoding` або поточного внутрішнього кодування в `to_encoding`. Також можна вказати необов'язковий параметр `from_encoding`. Якщо `string` є масивом (array), всі його рядкові (string) значення будуть перетворені рекурсивно.

### Список параметрів

`string`

Рядок (string) або масив (array), для перетворення.

`to_encoding`

Необхідне кодування результату.

`from_encoding`

Поточне кодування, яке використовується для інтерпретації рядка `string`. Декілька кодувань можуть бути вказані у вигляді масиву (array) або у вигляді рядка через кому, в цьому випадку правильне кодування буде визначено за тим же алгоритмом, що і функції [мбdetectencoding()](function.mb-detect-encoding.md)

Якщо параметр `from_encoding` дорівнює **`null`** або не вказано, то буде використовуватися [mbstring.internalencoding setting](mbstring.configuration.md#ini.mbstring.internal-encoding)якщо вона встановлена, інакше [кодировка по умолчанию](ini.core.md#ini.default-charset)

Допустимі значення `to_encoding` і `from_encoding` вказані на сторінці [кодування, що підтримуються](mbstring.supported-encodings.md)

### Значення, що повертаються

Перетворений рядок (string) або масив (array) або **`false`** у разі виникнення помилки.

### Помилки

Починаючи з PHP 8.0.0, якщо значення `to_encoding` або `from_encoding` є неприпустимим кодуванням, викидається [ValueError](class.valueerror.md). До PHP 8.0.0 натомість видавалася помилка рівня **`E_WARNING`**

### список змін

| Версия | Описание |
| --- | --- |
|  | **мбconvertencoding()** тепер викидає [ValueError](class.valueerror.md), якщо передано неприпустиме кодування в `to_encoding` |
|  | **мбconvertencoding()** тепер викидає [ValueError](class.valueerror.md), якщо передано неприпустиме кодування в `from_encoding` |
|  | Тепер `from_encoding` може бути **`null`** |
|  | Функція тепер також приймає масив (array) `string`. Раніше підтримувалися лише рядки (string). |

### Приклади

**Приклад #1 Приклад використання **мбconvertencoding()****

```php
<?php
/* Преобразует строку в кодировку SJIS */
$str = mb_convert_encoding($str, "SJIS");

/* Преобразует из EUC-JP в UTF-7 */
$str = mb_convert_encoding($str, "UTF-7", "EUC-JP");

/* Автоматически определяется кодировка среди JIS, eucjp-win, sjis-win, затем преобразуется в UCS-2LE */
$str = mb_convert_encoding($str, "UCS-2LE", "JIS, eucjp-win, sjis-win");

/* Если mbstring.language равен "Japanese", "auto" используется для обозначения "ASCII,JIS,UTF-8,EUC-JP,SJIS" */
$str = mb_convert_encoding($str, "EUC-JP", "auto");
?>
```

### Дивіться також

-   [мбdetectorder()](function.mb-detect-order.md) - Встановлення/отримання списку кодувань для механізмів визначення кодування
-   [UConverter::transcode()](uconverter.transcode.md) - Перетворює рядок з одного кодування символів на інший
-   [iconv()](function.iconv.md) - Перетворює рядок з одного кодування символів на інший
