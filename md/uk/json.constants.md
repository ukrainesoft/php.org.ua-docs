---
navigation:
  - json.resources.md: « Типи ресурсів
  - class.jsonexception.md: JsonException »
  - index.md: PHP Manual
  - book.json.md: JSON
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

Наступні константи вказують на тип помилки, повернутий функцією [json\_last\_error()](function.json-last-error.md) або зберігається, як code в [JsonException](class.jsonexception.md)

**`JSON_ERROR_NONE`**(int)

Не сталося жодних помилок.

**`JSON_ERROR_DEPTH`**(int)

Було перевищено максимальну глибину стека.

**`JSON_ERROR_STATE_MISMATCH`**(int)

Неправильний або пошкоджений JSON.

**`JSON_ERROR_CTRL_CHAR`**(int)

Помилка керуючих символів, ймовірно, через неправильне кодування.

**`JSON_ERROR_SYNTAX`**(int)

Синтаксична помилка.

**`JSON_ERROR_UTF8`**(int)

Пошкоджені символи UTF-8, ймовірно, через неправильне кодування.

**`JSON_ERROR_RECURSION`**(int)

Об'єкт або масив, переданий у функцію [json\_encode()](function.json-encode.md) включає рекурсивні посилання та не може бути закодований. Якщо було передано опцію **`JSON_PARTIAL_OUTPUT_ON_ERROR`**, то на місці рекурсивних посилань буде виведено **`null`**

**`JSON_ERROR_INF_OR_NAN`**(int)

Значение, переданное в функцию[json\_encode()](function.json-encode.md), включає або [**`NAN`**](language.types.float.md#language.types.float.nan), либо[**`INF`**](function.is-infinite.md). Якщо було вказано константу **`JSON_PARTIAL_OUTPUT_ON_ERROR`**, то замість зазначених особливих значень буде виведено

**`JSON_ERROR_UNSUPPORTED_TYPE`**(int)

У функцію [json\_encode()](function.json-encode.md) було передано значення непідтримуваного типу, наприклад, [resource](language.types.resource.md). Якщо було вказано константу **`JSON_PARTIAL_OUTPUT_ON_ERROR`**, то замість непідтримуваного значення виводитиметься **`null`**

**`JSON_ERROR_INVALID_PROPERTY_NAME`**(int)

У рядку переданому в [json\_decode()](function.json-decode.md) був ключ, що починається з символу \\u0000.

**`JSON_ERROR_UTF16`**(int)

Один непарний сурогат UTF-16 в екранованій послідовності Unicode у рядку JSON, переданому в [json\_decode()](function.json-decode.md)

Можна комбінувати наступні константи для передачі [json\_decode()](function.json-decode.md)

**`JSON_BIGINT_AS_STRING`**(int)

Декодує великі цілі числа як вихідне значення рядка.

**`JSON_OBJECT_AS_ARRAY`**(int)

Перетворює об'єкти JSON на масив PHP. Ця опція може бути задана автоматично, якщо викликати функцію [json\_decode()](function.json-decode.md), вказавши другим параметром значення **`true`**

Наступні константи можна комбінувати для використання в [json\_encode()](function.json-encode.md)

**`JSON_HEX_TAG`**(int)

Усі < і > кодуються в \\u003C и\\u003E.

**`JSON_HEX_AMP`**(int)

Всі & кодуються в \\u0026.

**`JSON_HEX_APOS`**(int)

Усі символи ' кодуються в \\u0027.

**`JSON_HEX_QUOT`**(int)

Усі символи "кодуються в \\u0022.

**`JSON_FORCE_OBJECT`**(int)

Видавати об'єкт замість масиву під час використання неасоціативного масиву. Це корисно, коли програма або код, що приймає, очікують об'єкт, а масив порожній.

**`JSON_NUMERIC_CHECK`**(int)

Кодування рядків, що містять числа, як числа.

**`JSON_PRETTY_PRINT`**(int)

Використовувати пробілові символи у даних, що повертаються для їх форматування.

**`JSON_UNESCAPED_SLASHES`**(int)

Не екранувати

**`JSON_UNESCAPED_UNICODE`**(int)

Не кодувати багатобайтові символи Unicode (за умовчанням вони кодуються як \\uXXXX).

**`JSON_PARTIAL_OUTPUT_ON_ERROR`**(int)

Дозволяє уникнути помилок при використанні функції json\_encode. Здійснює підстановку значень за замовчуванням замість некодованих.

**`JSON_PRESERVE_ZERO_FRACTION`**(int)

Гарантує, що значення типу float буде перетворено саме значення типу float у разі, якщо дробова частина дорівнює 0.

**`JSON_UNESCAPED_LINE_TERMINATORS`**(int)

Символи кінця рядка не будуть екрануватися, якщо задана константа **`JSON_UNESCAPED_UNICODE`**. Поведінка буде такою ж, якою вона була до PHP 7.1 без цієї константи. Доступно з PHP 7.1.0.

Наступні константи можна комбінувати для використання в [json\_decode()](function.json-decode.md) і [json\_encode()](function.json-encode.md)

**`JSON_INVALID_UTF8_IGNORE`**(int)

Ігнорувати неправильні символи UTF-8. Доступно з PHP 7.2.0.

**`JSON_INVALID_UTF8_SUBSTITUTE`**(int)

Перетворювати некоректні символи UTF-8 на \\0xfffd (Символ Юнікоду 'REPLACEMENT CHARACTER') Доступно з PHP 7.2.0.

**`JSON_THROW_ON_ERROR`**(int)

Викидається виняток [JsonException](class.jsonexception.md) у разі виникнення помилок замість встановлення глобального стану помилки, який можна отримати за допомогою функції [json\_last\_error()](function.json-last-error.md) і [json\_last\_error\_msg()](function.json-last-error-msg.md)Константа\*\*`JSON_PARTIAL_OUTPUT_ON_ERROR`**имеет приоритет над**`JSON_THROW_ON_ERROR`\*\*Доступно с PHP 7.3.0.
