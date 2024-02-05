---
navigation:
  - function.json-last-error-msg.md: « json\_last\_error\_msg
  - function.json-validate.md: json\_validate »
  - index.md: PHP Manual
  - ref.json.md: Функції JSON
title: json\_last\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# json\_last\_error

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

json\_last\_error — Повертає останню помилку

### Опис

```methodsynopsis
json_last_error(): int
```

Повертає останню помилку (якщо вона є), що сталася під час останнього кодування/декодування JSON, якщо під час виклику не використовувався прапор **`JSON_THROW_ON_ERROR`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле значення, яке може бути однією з наступних констант:

**Коди помилок JSON**

| Константа | Значение | Доступность |
| --- | --- | --- |
| **`JSON_ERROR_NONE`** | Помилок немає |  |
| **`JSON_ERROR_DEPTH`** | Досягнуто максимальної глибини стека |  |
| **`JSON_ERROR_STATE_MISMATCH`** | Неправильний або неправильний JSON |  |
| **`JSON_ERROR_CTRL_CHAR`** | Помилка символу керування, можливе неправильне кодування |  |
| **`JSON_ERROR_SYNTAX`** | Синтаксична помилка |  |
| **`JSON_ERROR_UTF8`** | Некоректні символи UTF-8, можливе неправильне кодування |  |
| **`JSON_ERROR_RECURSION`** | Одна або кілька зациклених посилань у значенні, що кодується |  |
| **`JSON_ERROR_INF_OR_NAN`** | Одне чи кілька значень [**`NAN`**](language.types.float.md#language.types.float.nan) або [**`INF`**](function.is-infinite.md) у кодованому значенні |  |
| **`JSON_ERROR_UNSUPPORTED_TYPE`** | Передано значення з непідтримуваним типом |  |
| **`JSON_ERROR_INVALID_PROPERTY_NAME`** | Ім'я властивості не може бути закодоване |  |
| **`JSON_ERROR_UTF16`** | Некоректний символ UTF-16, можливо, некоректно закодований |  |

### Приклади

**Пример #1 Пример использования**json\_last\_error()\*\*\*\*

```php
<?php
// Верная json-строка
$json[] = '{"Organization": "PHP Documentation Team"}';

// Неверная json-строка, которая вызовет синтаксическую ошибку,
// здесь в качестве кавычек мы используем ' вместо "
$json[] = "{'Organization': 'PHP Documentation Team'}";


foreach ($json as $string) {
    echo 'Декодируем: ' . $string;
    json_decode($string);

    switch (json_last_error()) {
        case JSON_ERROR_NONE:
            echo ' - Ошибок нет';
        break;
        case JSON_ERROR_DEPTH:
            echo ' - Достигнута максимальная глубина стека';
        break;
        case JSON_ERROR_STATE_MISMATCH:
            echo ' - Некорректные разряды или несоответствие режимов';
        break;
        case JSON_ERROR_CTRL_CHAR:
            echo ' - Некорректный управляющий символ';
        break;
        case JSON_ERROR_SYNTAX:
            echo ' - Синтаксическая ошибка, некорректный JSON';
        break;
        case JSON_ERROR_UTF8:
            echo ' - Некорректные символы UTF-8, возможно неверно закодирован';
        break;
        default:
            echo ' - Неизвестная ошибка';
        break;
    }

    echo PHP_EOL;
}
?>
```

Результат виконання наведеного прикладу:

```
Декодируем: {"Organization": "PHP Documentation Team"} - Ошибок нет
Декодируем: {'Organization': 'PHP Documentation Team'} - Синтаксическая ошибка, некорректный JSON
```

**Пример #2 Совместное использование**json\_last\_error()**и[json\_encode()](function.json-encode.md)**

```php
<?php
// Некорректная последовательность UTF8
$text = "\xB1\x31";

$json  = json_encode($text);
$error = json_last_error();

var_dump($json, $error === JSON_ERROR_UTF8);
?>
```

Результат виконання наведеного прикладу:

```
string(4) "null"
bool(true)
```

**Пример #3**json\_last\_error()**и**`JSON_THROW_ON_ERROR`\*\*\*\*

```php
<?php
// Некорректная последовательность UTF8, вызывающая JSON_ERROR_UTF8
json_encode("\xB1\x31");

// Не вызовет ошибки JSON
json_encode('okay', JSON_THROW_ON_ERROR);

// Глобальное состояние не будет изменено json_encode()
var_dump(json_last_error() === JSON_ERROR_UTF8);
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [json\_last\_error\_msg()](function.json-last-error-msg.md) \- Повертає рядок з повідомленням про помилку останнього дзвінка json\_encode() або json\_decode()
-   [json\_decode()](function.json-decode.md) \- Декодує рядок JSON
-   [json\_encode()](function.json-encode.md) \- Повертає JSON-подання даних
