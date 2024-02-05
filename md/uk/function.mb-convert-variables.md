---
navigation:
  - function.mb-convert-kana.md: « mb\_convert\_kana
  - function.mb-decode-mimeheader.md: mb\_decode\_mimeheader »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_convert\_variables
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_convert\_variables

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_convert\_variables — Перетворює символи на змінну з одного кодування на інше

### Опис

```methodsynopsis
mb_convert_variables(    string $to_encoding,    array|string $from_encoding,    mixed &$var,    mixed &...$vars): string|false
```

Конвертує символи в змінних `var`и`vars` з кодування, зазначеного у параметрі `from_encoding`, у кодування, зазначене у параметрі `to_encoding`

Функция**mb\_convert\_variables()** об'єднує рядки з масиву чи об'єкта визначення їх кодування, оскільки у разі коротких рядків визначити кодування часто вдається. Тому неприпустимо поміщати в один масив чи об'єкт рядка у різних кодуваннях.

### Список параметрів

`to_encoding`

Кодування, в яке потрібно перекодувати рядок (string).

`from_encoding`

Параметр`from_encoding` задається у вигляді масиву (array) або рядка (string) з розділеними комами кодуванням, функція спробує визначити кодування вихідного рядка на основі списку кодувань, заданих у параметрі `from-coding`. Якщо параметр `from_encoding` не заданий, буде обрано кодування, з INI-директиви з ім'ям `detect_order`

`var`

Параметр`var` - Це посилання на змінну, яку потрібно перетворити. Це може бути рядок (string), масив (array) чи об'єкт (object). Функція **mb\_convert\_variables()** передбачає, що всім параметрів задана однакова кодування.

`vars`

Додаткові `var`

### Значення, що повертаються

Повертає вихідне кодування у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования функции**mb\_convert\_variables()\*\*\*\*

```php
<?php
/* Преобразование переменных $post1, $post2 во внутреннюю кодировку скрипта */
$interenc = mb_internal_encoding();
$inputenc = mb_convert_variables($interenc, "ASCII,UTF-8,SJIS-win", $post1, $post2);
?>
```
