---
navigation:
  - function.mb-convert-case.md: « mb\_convert\_case
  - function.mb-convert-kana.md: mb\_convert\_kana »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_convert\_encoding
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_convert\_encoding

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_convert\_encoding — Перетворює рядок з одного кодування символів на інший

### Опис

```methodsynopsis
mb_convert_encoding(array|string $string, string $to_encoding, array|string|null $from_encoding = null): array|string|false
```

Перетворює значення параметра `string`из кодировки`from_encoding`, або поточного внутрішнього кодування, кодування `to_encoding`Если значение параметра`string` - це масив (array), всі його рядкові (string) значення будуть рекурсивно перетворені.

### Список параметрів

`string`

Рядок (string) або масив (array), для перетворення.

`to_encoding`

Необхідне кодування результату.

`from_encoding`

Поточне кодування, яке буде використане для інтерпретації рядка `string`. Кілька кодувань дозволено вказувати у вигляді масиву (array) або розділеного комами списку, тоді PHP спробує визначити правильне кодування за тим же алгоритмом, який використовує функція [mb\_detect\_encoding()](function.mb-detect-encoding.md)

Якщо параметр `from_encoding` опущений або дорівнює **`null`**, то буде використано значення директиви [mbstring.internal\_encoding setting](mbstring.configuration.md#ini.mbstring.internal-encoding), если она установлена, иначе[кодування за замовчуванням](ini.core.md#ini.default-charset)

Допустимі значення параметрів `to_encoding`и`from_encoding` вказані на сторінці [кодування, що підтримуються](mbstring.supported-encodings.md)

### Значення, що повертаються

Повертає перетворений рядок (string) або масив (array) або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Починаючи з PHP 8.0.0 викидається виняток [ValueError](class.valueerror.md), если значением параметра`to_encoding`или параметра`from_encoding` виявиться неприпустиме кодування. До PHP 8.0.0 натомість видавалася помилка рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Функция**mb\_convert\_encoding()** більше не повертатиме наступні нетекстові кодування: `«Base64»` `«QPrint»` `«UUencode»` `«HTML entities»` `«7 bit»`и`«8 bit»` |
| 8.0.0 | Функция**mb\_convert\_encoding()** тепер викидає виняток [ValueError](class.valueerror.md), якщо параметр `to_encoding` передане неприпустиме кодування. |
| 8.0.0 | Функция**mb\_convert\_encoding()** тепер викидає виняток [ValueError](class.valueerror.md), якщо параметр `from_encoding` передане неприпустиме кодування. |
| 8.0.0 | Тепер параметр `from_encoding` може набувати значення **`null`** |
| 7.2.0 | Функція тепер приймає масив (array) як параметр `string`. . Раніше підтримувалися лише рядки (string). |

### Приклади

**Приклад #1 Приклад використання функції** mb\_convert\_encoding()\*\*\*\*

```php
<?php

/* Преобразовывает строку в кодировку SJIS */
$str = mb_convert_encoding($str, "SJIS");

/* Преобразовывает из кодировки EUC-JP в кодировку UTF-7 */
$str = mb_convert_encoding($str, "UTF-7", "EUC-JP");

/* Автоматически определяется кодировка среди JIS, eucjp-win, sjis-win, затем преобразовывается в UCS-2LE */
$str = mb_convert_encoding($str, "UCS-2LE", "JIS, eucjp-win, sjis-win");

/* Если директива mbstring.language равна "Japanese", значение кодировки "auto" будет расширено до "ASCII,JIS,UTF-8,EUC-JP,SJIS" */
$str = mb_convert_encoding($str, "EUC-JP", "auto");
?>
```

### Дивіться також

-   [mb\_detect\_order()](function.mb-detect-order.md) \- Встановлює/отримує порядок визначення кодування символів
-   [UConverter::transcode()](uconverter.transcode.md) \- Перетворює рядок з одного кодування символів на інший
-   [iconv()](function.iconv.md) \- Перетворює рядок з одного кодування символів на інший
