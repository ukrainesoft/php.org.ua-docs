---
navigation:
  - function.json-decode.md: « json\_decode
  - function.json-last-error-msg.md: json\_last\_error\_msg »
  - index.md: PHP Manual
  - ref.json.md: Функції JSON
title: json\_encode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# json\_encode

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL json >= 1.2.0)

json\_encode — Повертає JSON-подання даних

### Опис

```methodsynopsis
json_encode(mixed $value, int $flags = 0, int $depth = 512): string|false
```

Повертає рядок, що містить JSON-подання для зазначеного `value`. Якщо параметр масивом (array) або об'єктом (object), він буде рекурсивно серіалізований.

Якщо значення, що серіалізується, є об'єктом, то за замовчуванням будуть включені тільки публічно видимі властивості. Як альтернатива клас може реалізувати інтерфейс [JsonSerializable](class.jsonserializable.md) для керування тим, як його значення серіалізуються в JSON.

На кодирование влияет параметр`flags`и, кроме того, кодирование значений типа float зависит от значения[serialize\_precision](ini.core.md#ini.serialize-precision)

### Список параметрів

`value`

`value` - значення, яке буде закодовано. Можливо будь-якого типу, крім [resource](language.types.resource.md)

Функція працює лише з кодуванням UTF-8.

> **Зауваження** :
> 
> PHP реалізує надмножина JSON, який описаний у початковому [» RFC 7159](http://www.faqs.org/rfcs/rfc7159)

`flags`

Бітова маска, що складається із значень **`JSON_FORCE_OBJECT`** **`JSON_HEX_QUOT`** **`JSON_HEX_TAG`** **`JSON_HEX_AMP`** **`JSON_HEX_APOS`** **`JSON_INVALID_UTF8_IGNORE`** **`JSON_INVALID_UTF8_SUBSTITUTE`** **`JSON_NUMERIC_CHECK`** **`JSON_PARTIAL_OUTPUT_ON_ERROR`** **`JSON_PRESERVE_ZERO_FRACTION`** **`JSON_PRETTY_PRINT`** **`JSON_UNESCAPED_LINE_TERMINATORS`** **`JSON_UNESCAPED_SLASHES`** **`JSON_UNESCAPED_UNICODE`** **`JSON_THROW_ON_ERROR`**. Сенс цих констант пояснюється на [сторінці JSON-констант](json.constants.md)

`depth`

Встановлює максимальну глибину. Має бути більше нуля.

### Значення, що повертаються

Повертає рядок (string), закодований JSON або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.3.0 | Добавлена константа\*\*`JSON_THROW_ON_ERROR`\*\*для параметра`flags` |
| 7.2.0 | Додані константи \*\*`JSON_INVALID_UTF8_IGNORE`** і **`JSON_INVALID_UTF8_SUBSTITUTE`\*\*для параметра`flags` |
| 7.1.0 | Добавлена константа\*\*`JSON_UNESCAPED_LINE_TERMINATORS`\*\*для параметра`flags` |
| 7.1.0 | При кодуванні чисел із плаваючою точкою (float) використовується [serialize\_precision](ini.core.md#ini.serialize-precision) замість [precision](ini.core.md#ini.precision) |

### Приклади

**Приклад #1 Приклад використання** json\_encode()\*\*\*\*

```php
<?php
$arr = array('a' => 1, 'b' => 2, 'c' => 3, 'd' => 4, 'e' => 5);

echo json_encode($arr);
?>
```

Результат виконання наведеного прикладу:

```
{"a":1,"b":2,"c":3,"d":4,"e":5}
```

**Приклад #2 Приклад використання** json\_encode()\*\* з опціями\*\*

```php
<?php
$a = array('<foo>',"'bar'",'"baz"','&blong&', "\xc3\xa9");

echo "Обычно: ",     json_encode($a), "\n";
echo "Теги: ",       json_encode($a, JSON_HEX_TAG), "\n";
echo "Апострофы: ",  json_encode($a, JSON_HEX_APOS), "\n";
echo "Кавычки: ",    json_encode($a, JSON_HEX_QUOT), "\n";
echo "Амперсанды: ", json_encode($a, JSON_HEX_AMP), "\n";
echo "Юникод: ",     json_encode($a, JSON_UNESCAPED_UNICODE), "\n";
echo "Все: ",        json_encode($a, JSON_HEX_TAG | JSON_HEX_APOS | JSON_HEX_QUOT | JSON_HEX_AMP | JSON_UNESCAPED_UNICODE), "\n\n";

$b = array();

echo "Отображение пустого массива как массива: ", json_encode($b), "\n";
echo "Отображение неассоциативного массива как объекта: ", json_encode($b, JSON_FORCE_OBJECT), "\n\n";

$c = array(array(1,2,3));

echo "Отображение неассоциативного массива как массива: ", json_encode($c), "\n";
echo "Отображение неассоциативного массива как объекта: ", json_encode($c, JSON_FORCE_OBJECT), "\n\n";

$d = array('foo' => 'bar', 'baz' => 'long');

echo "Ассоциативный массив всегда отображается как объект: ", json_encode($d), "\n";
echo "Ассоциативный массив всегда отображается как объект: ", json_encode($d, JSON_FORCE_OBJECT), "\n\n";
?>
```

Результат виконання наведеного прикладу:

```
Обычно: ["<foo>","'bar'","\"baz\"","&blong&","\u00e9"]
Теги: ["\u003Cfoo\u003E","'bar'","\"baz\"","&blong&","\u00e9"]
Апострофы: ["<foo>","\u0027bar\u0027","\"baz\"","&blong&","\u00e9"]
Кавычки: ["<foo>","'bar'","\u0022baz\u0022","&blong&","\u00e9"]
Амперсанды: ["<foo>","'bar'","\"baz\"","\u0026blong\u0026","\u00e9"]
Юникод: ["<foo>","'bar'","\"baz\"","&blong&","é"]
Все: ["\u003Cfoo\u003E","\u0027bar\u0027","\u0022baz\u0022","\u0026blong\u0026","é"]

Отображение пустого массива как массива: []
Отображение неассоциативного массива как объекта: {}

Отображение неассоциативного массива как массива: [[1,2,3]]
Отображение неассоциативного массива как объекта: {"0":{"0":1,"1":2,"2":3}}

Ассоциативный массив всегда отображается как объект: {"foo":"bar","baz":"long"}
Ассоциативный массив всегда отображается как объект: {"foo":"bar","baz":"long"}
```

**Приклад #3 Приклад використання опції JSON\_NUMERIC\_CHECK**

```php
<?php
echo "Строки, содержащие числа преобразуются в числа".PHP_EOL;
$numbers = array('+123123', '-123123', '1.2e3', '0.00001');
var_dump(
 $numbers,
 json_encode($numbers, JSON_NUMERIC_CHECK)
);
echo "Строки, содержащие некорректно заданные числа".PHP_EOL;
$strings = array('+a33123456789', 'a123');
var_dump(
 $strings,
 json_encode($strings, JSON_NUMERIC_CHECK)
);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Строки, содержащие числа преобразуются в числа
array(4) {
  [0]=>
  string(7) "+123123"
  [1]=>
  string(7) "-123123"
  [2]=>
  string(5) "1.2e3"
  [3]=>
  string(7) "0.00001"
}
string(28) "[123123,-123123,1200,1.0e-5]"
Строки, содержащие некорректно заданные числа
array(2) {
  [0]=>
  string(13) "+a33123456789"
  [1]=>
  string(4) "a123"
}
string(24) "["+a33123456789","a123"]"
```

**Приклад #4 Приклад з послідовними індексами, що починаються з нуля, та непослідовними індексами масивів**

```php
<?php
echo "Последовательный массив".PHP_EOL;
$sequential = array("foo", "bar", "baz", "blong");
var_dump(
 $sequential,
 json_encode($sequential)
);

echo PHP_EOL."Непоследовательный массив".PHP_EOL;
$nonsequential = array(1=>"foo", 2=>"bar", 3=>"baz", 4=>"blong");
var_dump(
 $nonsequential,
 json_encode($nonsequential)
);

echo PHP_EOL."Последовательный массив с одним удалённым индексом".PHP_EOL;
unset($sequential[1]);
var_dump(
 $sequential,
 json_encode($sequential)
);
?>
```

Результат виконання наведеного прикладу:

```
Последовательный массив
array(4) {
  [0]=>
  string(3) "foo"
  [1]=>
  string(3) "bar"
  [2]=>
  string(3) "baz"
  [3]=>
  string(5) "blong"
}
string(27) "["foo","bar","baz","blong"]"

Непоследовательный массив
array(4) {
  [1]=>
  string(3) "foo"
  [2]=>
  string(3) "bar"
  [3]=>
  string(3) "baz"
  [4]=>
  string(5) "blong"
}
string(43) "{"1":"foo","2":"bar","3":"baz","4":"blong"}"

Последовательный массив с одним удалённым индексом
array(3) {
  [0]=>
  string(3) "foo"
  [2]=>
  string(3) "baz"
  [3]=>
  string(5) "blong"
}
string(33) "{"0":"foo","2":"baz","3":"blong"}"
```

**Приклад #5 Приклад использования опции**`JSON_PRESERVE_ZERO_FRACTION`\*\*\*\*

```php
<?php
var_dump(json_encode(12.0, JSON_PRESERVE_ZERO_FRACTION));
var_dump(json_encode(12.0));
?>
```

Результат виконання наведеного прикладу:

```
string(4) "12.0"
string(2) "12"
```

### Примітки

> **Зауваження** :
> 
> у разі виникнення помилки кодування можна використовувати [json\_last\_error()](function.json-last-error.md) визначення точної помилки.

> **Зауваження** :
> 
> При кодуванні масиву у разі, якщо його індекси не є послідовними числами від нуля, всі індекси кодуються в рядкові ключі для кожної пари індекс-значення.

> **Зауваження** :
> 
> Як і еталонний кодувальник JSON, **json\_encode()** буде створювати JSON у вигляді простого значення (тобто не об'єкт і не масив), якщо йому передані типи string, int, float або bool як вхідне значення `value`. Більшість декодерів сприймають ці значення як правильний JSON, але деякі ні, тому що специфікація неоднозначна щодо цього.
> 
> Завжди перевіряйте, що ваш декодер JSON може правильно обробляти дані, які ви створюєте за допомогою **json\_encode()**

### Дивіться також

-   [JsonSerializable](class.jsonserializable.md)
-   [json\_decode()](function.json-decode.md) \- Декодує рядок JSON
-   [json\_last\_error()](function.json-last-error.md) \- Повертає останню помилку
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
