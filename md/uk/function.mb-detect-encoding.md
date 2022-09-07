---
navigation:
  - function.mb-decode-numericentity.md: « mbdecodenumericentity
  - function.mb-detect-order.md: мбdetectorder »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбdetectencoding
---
# мбdetectencoding

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбdetectencoding — Визначення кодування символів

### Опис

```methodsynopsis
mb_detect_encoding(string $string, array|string|null $encodings = null, bool $strict = false): string|false
```

Визначає найімовірніше кодування символів для рядка (string) `string` із упорядкованого списку кандидатів.

Автоматичне визначення передбачуваного кодування символів може бути повністю надійним; без додаткової інформації це схоже на розшифрування зашифрованого рядка без ключа. Завжди бажано використовувати індикацію кодування символів, що зберігається або передається з даними, таку як заголовок HTTP "Content-Type".

Функція найбільш корисна з багатобайтовим кодуванням, коли не всі послідовності байтів утворюють допустимий рядок. Якщо вхідний рядок містить таку послідовність, це кодування буде відхилено, і буде перевірено наступне кодування.

### Список параметрів

`string`

Перевірений рядок (string).

`encodings`

Упорядкований список символів кодування. Список може бути вказаний як масив рядків або як рядок кодувань, розділених комами.

Якщо `encodings` не заданий чи є **`null`**, буде використовуватись поточний detectorder (встановлений за допомогою параметра конфігурації [mbstring.detectorder](mbstring.configuration.md#ini.mbstring.detect-order) або функції [мбdetectorder()](function.mb-detect-order.md)

`strict`

Керує поведінкою, коли `string` неприпустима в жодній із перерахованих `encodings`. Якщо для `strict` встановлено значення **`false`**, буде повернуто найбільш відповідне кодування; якщо для `strict` встановлено значення **`true`**, буде повернуто **`false`**

Значення за замовчуванням для `strict` можна встановити за допомогою параметра конфігурації [mbstring.strictdetection](mbstring.configuration.md#ini.mbstring.strict-detection)

### Значення, що повертаються

Назва кодування символів або **`false`**, якщо рядок неприпустимий в жодному з перерахованих кодувань.

### Приклади

**Приклад #1 Приклад використання **мбdetectencoding()****

```php
<?php
// Определение кодировки с текущим detect_order
echo mb_detect_encoding($str);

// "auto" раскрывается в соответствии с mbstring.language
echo mb_detect_encoding($str, "auto");

// Зададим список кодировок "encodings" в виде строки
echo mb_detect_encoding($str, "JIS, eucjp-win, sjis-win");

// Использование Масива для задания возможных кодировок "encodings"
$encodings = [
  "ASCII",
  "JIS",
  "EUC-JP"
];
echo mb_detect_encoding($str, $encodings);
?>
```

**Приклад #2 Дія параметра `strict`**

```php
<?php
// 'áéóú' закодирована в ISO-8859-1
$str = "\xE1\xE9\xF3\xFA";

// Строка недействительна в ASCII или UTF-8, но UTF-8 считается более близким соответствием
var_dump(mb_detect_encoding($str, ['ASCII', 'UTF-8'], false));
var_dump(mb_detect_encoding($str, ['ASCII', 'UTF-8'], true));

// Если допустимая кодировка найдена, параметр strict не меняет результат
var_dump(mb_detect_encoding($str, ['ASCII', 'UTF-8', 'ISO-8859-1'], false));
var_dump(mb_detect_encoding($str, ['ASCII', 'UTF-8', 'ISO-8859-1'], true));
?>
```

Результат виконання цього прикладу:

```
string(5) "UTF-8"
bool(false)
string(10) "ISO-8859-1"
string(10) "ISO-8859-1"
```

У деяких випадках та сама послідовність байтів може утворювати допустимий рядок у кількох кодуваннях символів, і неможливо дізнатися, яка інтерпретація призначалася. Наприклад, серед багатьох інших байтова послідовністьxC4xA2" може бути:

-   "Ä¢" (U+00C4 LATIN CAPITAL LETTER A WITH DIAERESIS з наступним U+00A2 CENT SIGN) закодована в ISO-8859-1, ISO-8859-15 або Windows-1252
-   "ФЂ" (U+0424 CYRILLIC CAPITAL LETTER EF з наступним U+0402 CYRILLIC CAPITAL LETTER DJE) закодована ISO-8859-5
-   "C" (U+0122 LATIN CAPITAL LETTER G WITH CEDILLA) закодована в UTF-8

**Приклад #3 Використання порядку при збігу кількох кодувань**

```php
<?php
$str = "\xC4\xA2";

// Строка действительна во всех трех кодировках, поэтому будет возвращена первая из перечисленных кодировок.
var_dump(mb_detect_encoding($str, ['UTF-8', 'ISO-8859-1', 'ISO-8859-5']));
var_dump(mb_detect_encoding($str, ['ISO-8859-1', 'ISO-8859-5', 'UTF-8']));
var_dump(mb_detect_encoding($str, ['ISO-8859-5', 'UTF-8', 'ISO-8859-1']));
?>
```

Результат виконання цього прикладу:

```
string(5) "UTF-8"
string(10) "ISO-8859-1"
string(10) "ISO-8859-5"
```

### Дивіться також

-   [мбdetectorder()](function.mb-detect-order.md) - Встановлення/отримання списку кодувань для механізмів визначення кодування
