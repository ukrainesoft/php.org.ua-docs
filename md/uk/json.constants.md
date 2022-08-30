Обумовлені константи

-   [« Типы ресурсов](json.resources.html)
    
-   [JsonException »](class.jsonexception.html)
    
-   [PHP Manual](index.html)
    
-   [JSON](book.json.html)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

Наступні константи вказують на тип помилки, повернутий функцією [jsonlasterror()](function.json-last-error.html) або зберігається, як code в [JsonException](class.jsonexception.html)

**`JSON_ERROR_NONE`** (int)

Не сталося жодних помилок.

**`JSON_ERROR_DEPTH`** (int)

Було перевищено максимальну глибину стека.

**`JSON_ERROR_STATE_MISMATCH`** (int)

Неправильний або пошкоджений JSON.

**`JSON_ERROR_CTRL_CHAR`** (int)

Помилка керуючих символів, ймовірно, через неправильне кодування.

**`JSON_ERROR_SYNTAX`** (int)

Синтаксична помилка.

**`JSON_ERROR_UTF8`** (int)

Пошкоджені символи UTF-8, ймовірно, через неправильне кодування.

**`JSON_ERROR_RECURSION`** (int)

Об'єкт або масив, переданий у функцію [jsonencode()](function.json-encode.html) включає рекурсивні посилання та не може бути закодований. Якщо було передано опцію **`JSON_PARTIAL_OUTPUT_ON_ERROR`**, то на місці рекурсивних посилань буде виведено **`null`**

**`JSON_ERROR_INF_OR_NAN`** (int)

Значення, передане у функцію [jsonencode()](function.json-encode.html), включає або [**`NAN`**](language.types.float.html#language.types.float.nan), або [**`INF`**](function.is-infinite.html). Якщо було вказано константу **`JSON_PARTIAL_OUTPUT_ON_ERROR`**, то замість зазначених особливих значень буде виведено `0`

**`JSON_ERROR_UNSUPPORTED_TYPE`** (int)

У функцію [jsonencode()](function.json-encode.html) було передано значення непідтримуваного типу, наприклад, [resource](language.types.resource.html). Якщо було вказано константу **`JSON_PARTIAL_OUTPUT_ON_ERROR`**, то замість непідтримуваного значення виводитиметься **`null`**

**`JSON_ERROR_INVALID_PROPERTY_NAME`** (int)

У рядку переданому в [jsondecode()](function.json-decode.html) був ключ, що починається з символу u0000.

**`JSON_ERROR_UTF16`** (int)

Один непарний сурогат UTF-16 в екранованій послідовності Unicode у рядку JSON, переданому в [jsondecode()](function.json-decode.html)

Можна комбінувати наступні константи для передачі [jsondecode()](function.json-decode.html)

**`JSON_BIGINT_AS_STRING`** (int)

Декодує великі цілі числа як вихідне значення рядка.

**`JSON_OBJECT_AS_ARRAY`** (int)

Перетворює об'єкти JSON на масив PHP. Ця опція може бути задана автоматично, якщо викликати [jsondecode()](function.json-decode.html) вказавши другим параметром **`true`**

Наступні константи можна комбінувати для використання в [jsonencode()](function.json-encode.html)

**`JSON_HEX_TAG`** (int)

Всі кодуються в u003C та u003E.

**`JSON_HEX_AMP`** (int)

Всі & кодуються в u0026.

**`JSON_HEX_APOS`** (int)

Усі символи ' кодуються в u0027.

**`JSON_HEX_QUOT`** (int)

Усі символи "кодуються в u0022.

**`JSON_FORCE_OBJECT`** (int)

Видавати об'єкт замість масиву під час використання неасоціативного масиву. Це корисно, коли програма або код, що приймає, очікують об'єкт, а масив порожній.

**`JSON_NUMERIC_CHECK`** (int)

Кодування рядків, що містять числа, як числа.

**`JSON_PRETTY_PRINT`** (int)

Використовувати пробілові символи у даних, що повертаються для їх форматування.

**`JSON_UNESCAPED_SLASHES`** (int)

Не екранувати `/`

**`JSON_UNESCAPED_UNICODE`** (int)

Не кодувати багатобайтові символи Unicode (за замовчуванням вони кодуються як uXXXX).

**`JSON_PARTIAL_OUTPUT_ON_ERROR`** (int)

Дозволяє уникнути помилок при використанні функції jsonencode. Здійснює підстановку значень за замовчуванням замість некодованих.

**`JSON_PRESERVE_ZERO_FRACTION`** (int)

Гарантує, що значення типу float буде перетворено саме значення типу float у разі, якщо дробова частина дорівнює 0.

**`JSON_UNESCAPED_LINE_TERMINATORS`** (int)

Символи кінця рядка не будуть екрануватися, якщо задана константа **`JSON_UNESCAPED_UNICODE`**. Поведінка буде такою ж, якою вона була до PHP 7.1 без цієї константи. Доступно з PHP 7.1.0.

Наступні константи можна комбінувати для використання в [jsondecode()](function.json-decode.html) і [jsonencode()](function.json-encode.html)

**`JSON_INVALID_UTF8_IGNORE`** (int)

Ігнорувати неправильні символи UTF-8. Доступно з PHP 7.2.0.

**`JSON_INVALID_UTF8_SUBSTITUTE`** (int)

Перетворювати некоректні символи UTF-8 на 0xfffd (Символ Юнікоду 'REPLACEMENT CHARACTER') Доступно з PHP 7.2.0.

**`JSON_THROW_ON_ERROR`** (int)

Викидається виняток [JsonException](class.jsonexception.html) у разі виникнення помилок замість встановлення глобального стану помилки, який можна отримати за допомогою функції [jsonlasterror()](function.json-last-error.html) і [jsonlasterrormsg()](function.json-last-error-msg.html). Константа **`JSON_PARTIAL_OUTPUT_ON_ERROR`** має пріоритет над **`JSON_THROW_ON_ERROR`**. Доступно з PHP 7.3.0.