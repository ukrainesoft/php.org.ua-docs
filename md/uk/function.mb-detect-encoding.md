---
navigation:
  - function.mb-decode-numericentity.md: « mb\_decode\_numericentity
  - function.mb-detect-order.md: mb\_detect\_order »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_detect\_encoding
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_detect\_encoding

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_detect\_encoding — Визначає кодування символів

### Опис

```methodsynopsis
mb_detect_encoding(string $string, array|string|null $encodings = null, bool $strict = false): string|false
```

Визначає найімовірніше кодування символів рядка, переданого в параметр `string`, перевіряючи список кандидатів у порядку.

Автоматичне визначення передбачуваного кодування символів не є надійним; без додаткової інформації це схоже на розшифрування зашифрованого рядка без ключа. Краще вказати кодування символів, що зберігається або передається з даними, наприклад в HTTP-заголовку Content-Type.

Функція буде корисніша, якщо викликати її з багатобайтовими кодуваннями, оскільки не всі послідовності байтів утворюють допустимий рядок. Якщо вхідний рядок містить таку послідовність, кодування буде відхилено, і буде перевірено наступне кодування.

### Список параметрів

`string`

Перевірений рядок (string).

`encodings`

Список коду символів для перевірки в заданому порядку. Список може бути визначений як масив рядків або як один рядок, розділений комами.

Якщо параметр `encodings` не заданий або дорівнює **`null`**, буде вибрано кодування, встановлене в директиві з ім'ям detect\_order (устанавливают в директиве[mbstring.detect\_order](mbstring.configuration.md#ini.mbstring.detect-order) налаштувань конфігурації або функції [mb\_detect\_order()](function.mb-detect-order.md)

`strict`

Управляет поведением, когда строка в параметре`string` неприпустима для жодної перерахованої у параметрі `encodings` кодування. Якщо параметр `strict`установлен в значение\*\*`false`**, буде повернуто перше збіглося кодування; якщо параметр `strict`установлен в значение**`true`\*\*, буде повернено значення **`false`**

Значение по умолчанию для параметра`strict`можно установить в директиве[mbstring.strict\_detection](mbstring.configuration.md#ini.mbstring.strict-detection) налаштувань конфігурації.

### Значення, що повертаються

Повертає виявлене кодування символів або **`false`**, якщо рядок неприпустимий для жодного з перерахованих кодувань.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Функция**mb\_detect\_encoding()** більше не повертатиме наступні нетекстові кодування: `«Base64»` `«QPrint»` `«UUencode»` `«HTML entities»` `«7 bit»`и`«8 bit»` |

### Приклади

**Пример #1 Пример использования функции**mb\_detect\_encoding()\*\*\*\*

```php
<?php

// Определение кодировки с текущей detect_order
echo mb_detect_encoding($str);

// Значение «auto» раскрывается в соответствии с директивой mbstring.language
echo mb_detect_encoding($str, "auto");

// Установка параметра «encodings» списком, разделённым запятой
echo mb_detect_encoding($str, "JIS, eucjp-win, sjis-win");

// Установка параметра «encodings» массивом
$encodings = [
  "ASCII",
  "JIS",
  "EUC-JP"
];
echo mb_detect_encoding($str, $encodings);
```

**Пример #2 Действие параметра`strict`**

```php
<?php

// «áéóú» закодирована в ISO-8859-1
$str = "\xE1\xE9\xF3\xFA";

// Строка недействительна для кодировок ASCII или UTF-8, но UTF-8 считается более близким соответствием
var_dump(mb_detect_encoding($str, ['ASCII', 'UTF-8'], false));
var_dump(mb_detect_encoding($str, ['ASCII', 'UTF-8'], true));

// Если допустимая кодировка найдена, параметр strict не меняет результат
var_dump(mb_detect_encoding($str, ['ASCII', 'UTF-8', 'ISO-8859-1'], false));
var_dump(mb_detect_encoding($str, ['ASCII', 'UTF-8', 'ISO-8859-1'], true));
```

Результат виконання наведеного прикладу:

```
string(5) "UTF-8"
bool(false)
string(10) "ISO-8859-1"
string(10) "ISO-8859-1"
```

Іноді та сама послідовність байтів може утворювати допустимий рядок у кількох кодуваннях символів, і неможливо дізнатися, яка інтерпретація передбачалася. Наприклад, серед багатьох інших байтова послідовність\\xC4\\xA2» може бути:

-   Ä¢ (U+00C4 LATIN CAPITAL LETTER A WITH DIAERESIS з наступним U+00A2 CENT SIGN), закодована в одному з кодувань - ISO-8859-1, ISO-8859-15 або Windows-1252
-   "ФЂ" (U+0424 CYRILLIC CAPITAL LETTER EF з наступним U+0402 CYRILLIC CAPITAL LETTER DJE), закодована ISO-8859-5
-   «»» (U+0122 LATIN CAPITAL LETTER G WITH CEDILLA), закодована в UTF-8

**Приклад #3 Дія порядку кодувань при збігу кількох кандидатів**

```php
<?php

$str = "\xC4\xA2";

// Строка действительна во всех трёх кодировках, поэтому будет возвращена первая из перечисленных кодировок
var_dump(mb_detect_encoding($str, ['UTF-8', 'ISO-8859-1', 'ISO-8859-5']));
var_dump(mb_detect_encoding($str, ['ISO-8859-1', 'ISO-8859-5', 'UTF-8']));
var_dump(mb_detect_encoding($str, ['ISO-8859-5', 'UTF-8', 'ISO-8859-1']));
?>
```

Результат виконання наведеного прикладу:

```
string(5) "UTF-8"
string(10) "ISO-8859-1"
string(10) "ISO-8859-5"
```

### Дивіться також

-   [mb\_detect\_order()](function.mb-detect-order.md) \- Встановлює/отримує порядок визначення кодування символів
