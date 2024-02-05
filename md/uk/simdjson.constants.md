---
navigation:
  - simdjson.installation.md: « Встановлення
  - ref.simdjson.md: Функції Simdjson »
  - index.md: PHP Manual
  - book.simdjson.md: Simdjson
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`SIMDJSON_ERR_CAPACITY`**(int)

Синтаксичний аналізатор не підтримує такого розміру документ. Викидається при розборі рядка JSON довжиною понад 4 Гб.

**`SIMDJSON_ERR_TAPE_ERROR`**(int)

У JSON-документа неправильна структура: відсутні або зайві коми, дужки, пропущені ключі і т.д.

**`SIMDJSON_ERR_DEPTH_ERROR`**(int)

JSON-документ занадто глибокий (занадто багато вкладених об'єктів та масивів).

**`SIMDJSON_ERR_STRING_ERROR`**(int)

Проблема при розборі рядка.

**`SIMDJSON_ERR_T_ATOM_ERROR`**(int)

Проблема при розборі атома, що починається з літери t.

**`SIMDJSON_ERR_F_ATOM_ERROR`**(int)

Проблема при аналізі атома, що починається з літери 'f'.

**`SIMDJSON_ERR_N_ATOM_ERROR`**(int)

Проблема при аналізі атома, що починається з літери 'n'.

**`SIMDJSON_ERR_NUMBER_ERROR`**(int)

Проблема при розборі числа.

**`SIMDJSON_ERR_UTF8_ERROR`**(int)

Вхідні дані не відповідають стандарту UTF-8.

**`SIMDJSON_ERR_UNINITIALIZED`**(int)

Парсер, який використовується simdjson, не ініціалізований. Цього не має відбуватися.

**`SIMDJSON_ERR_EMPTY`**(int)

Порожньо: JSON не знайдено.

**`SIMDJSON_ERR_UNESCAPED_CHARS`**(int)

У рядках деякі символи мають бути екрановані, але неекрановані символи.

**`SIMDJSON_ERR_UNCLOSED_STRING`**(int)

Рядок відкривається, але ніколи не закривається.

**`SIMDJSON_ERR_UNSUPPORTED_ARCHITECTURE`**(int)

У simdjson немає реалізації, що підтримується даною архітектурою CPU (можливо, це не SIMD CPU?).

**`SIMDJSON_ERR_INCORRECT_TYPE`**(int)

Цього не має статися.

**`SIMDJSON_ERR_NUMBER_OUT_OF_RANGE`**(int)

Число JSON занадто велике або занадто маленьке, щоб вписатися в тип, що запитується. Зауважте, що бібліотека C simdjson є форком і ця помилка ігнорується, щоб відповідати обробці PHP занадто великих чи занадто маленьких чисел JSON.

**`SIMDJSON_ERR_INDEX_OUT_OF_BOUNDS`**(int)

Цього не має статися.

**`SIMDJSON_ERR_NO_SUCH_FIELD`**(int)

Цього не має статися.

**`SIMDJSON_ERR_IO_ERROR`**(int)

Цього не має статися.

**`SIMDJSON_ERR_INVALID_JSON_POINTER`**(int)

Неправильний синтаксис вказівника JSON у функції [simdjson\_key\_value()](function.simdjson-key-value.md) та інших функціях, які приймають покажчик JSON $key.

**`SIMDJSON_ERR_INVALID_URI_FRAGMENT`**(int)

Неправильний синтаксис фрагмента URI.

**`SIMDJSON_ERR_UNEXPECTED_ERROR`**(int)

Непередбачена помилка, подумайте про те, щоб повідомити про цю проблему, оскільки, можливо, ви знайшли помилку в simdjson PECL.

**`SIMDJSON_ERR_PARSER_IN_USE`**(int)

Цього не має статися.

**`SIMDJSON_ERR_OUT_OF_ORDER_ITERATION`**(int)

Цього не має статися.

**`SIMDJSON_ERR_INSUFFICIENT_PADDING`**(int)

Цього не має статися.

**`SIMDJSON_ERR_INCOMPLETE_ARRAY_OR_OBJECT`**(int)

Документ JSON закінчився передчасно всередині об'єкта або масиву.

**`SIMDJSON_ERR_SCALAR_DOCUMENT_AS_VALUE`**(int)

Цього не має статися.

**`SIMDJSON_ERR_OUT_OF_BOUNDS`**(int)

Спроба доступу до розташування поза документом.

**`SIMDJSON_ERR_TRAILING_CONTENT`**(int)

**`SIMDJSON_ERR_KEY_COUNT_NOT_COUNTABLE`**(int)

**`SIMDJSON_ERR_INVALID_PROPERTY`**(int)

Недопустимое имя свойства для[stdClass](class.stdclass.md)при декодировании значения с помощью функции[simdjson\_decode()](function.simdjson-decode.md) або [simdjson\_key\_value()](function.simdjson-key-value.md)
