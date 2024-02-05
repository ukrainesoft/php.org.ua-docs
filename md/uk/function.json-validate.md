---
navigation:
  - function.json-last-error.md: « json\_last\_error
  - book.simdjson.md: Simdjson »
  - index.md: PHP Manual
  - ref.json.md: Функції JSON
title: json\_validate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# json\_validate

(PHP 8 >= 8.3.0)

json\_validate — Перевіряє, чи має рядок допустимий JSON

### Опис

```methodsynopsis
json_validate(string $json, int $depth = 512, int $flags = 0): bool
```

Повертає результат перевірки відповідності формату вхідного рядка (string) допустимому JSON. Якщо функція **json\_validate()** поверне **`true`**, функция[json\_decode()](function.json-decode.md)успешно декодирует входную строку при использовании тех же параметров`depth`и`flags`

Якщо функція **json\_validate()** поверне **`false`**, причину можно будет установить с помощью функции[json\_last\_error()](function.json-last-error.md) і [json\_last\_error\_msg()](function.json-last-error-msg.md)

Функция\*\*json\_validate()\*\*использует меньше памяти, чем функция[json\_decode()](function.json-decode.md), оскільки їй не потрібно декодувати корисне навантаження JSON або створювати структуру масиву або об'єкта, що містить її.

**Застереження**

Виклик функції \*\*json\_validate()\*\*непосредственно перед функцией[json\_decode()](function.json-decode.md) призведе до непотрібного подвійного аналізу рядка, оскільки функція [json\_decode()](function.json-decode.md) неявно виконує таку перевірку під час декодування.

Використати функцію **json\_validate()** треба тільки у випадку, коли дані декодування корисного навантаження JSON не потрібно використовувати негайно, і необхідно знати, чи містить рядок допустимий JSON.

### Список параметрів

`json`

Рядок для перевірки.

Ця функція працює тільки з рядками кодування UTF-8.

> **Зауваження** :
> 
> PHP реалізує надмножина JSON, який описаний у початковому [» RFC 7159](http://www.faqs.org/rfcs/rfc7159)

`depth`

Максимальна глибина вкладеності структури, на яку проводитиметься декодування. Значення має бути більшим і менше чи одно `2147483647`

`flags`

В даний час приймається тільки **`JSON_INVALID_UTF8_IGNORE`**

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо вхідний рядок є синтаксично допустимим JSON, або **`false`** в іншому випадку.

### Помилки

Если значение параметра`depth` виходить за межі допустимого діапазону, буде викинуто виняток [ValueError](class.valueerror.md)

Если значение параметра`flags`— неприпустимий прапор, буде викинуто виняток [ValueError](class.valueerror.md)

### Приклади

**Пример #1 Пример использования**json\_validate()\*\*\*\*

```php
<?php
var_dump(json_validate('{ "test": { "foo": "bar" } }'));
var_dump(json_validate('{ "": "": "" } }'));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [json\_decode()](function.json-decode.md) \- Декодує рядок JSON
-   [json\_last\_error()](function.json-last-error.md) \- Повертає останню помилку
-   [json\_last\_error\_msg()](function.json-last-error-msg.md) \- Повертає рядок з повідомленням про помилку останнього дзвінка json\_encode() або json\_decode()
