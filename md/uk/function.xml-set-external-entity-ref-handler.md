---
navigation:
  - function.xml-set-end-namespace-decl-handler.md: « xml\_set\_end\_namespace\_decl\_handler
  - function.xml-set-notation-decl-handler.md: xml\_set\_notation\_decl\_handler »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_set\_external\_entity\_ref\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_set\_external\_entity\_ref\_handler

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_set\_external\_entity\_ref\_handler - Встановлення обробника зовнішніх сутностей

### Опис

```methodsynopsis
xml_set_external_entity_ref_handler(XMLParser $parser, callable $handler): true
```

Задає функцію обробник зовнішніх сутностей для XML-аналізатора `parser`

### Список параметрів

`parser`

Парсер XML.

`handler`

Якщо передається значення **`null`** або порожній рядок, обробник повертається в стан за замовчуванням.

Якщо параметр `handler` є типом [callable](language.types.callable.md), то як оброблювач встановлюється callable.

Якщо параметр `handler` є рядком (string), це може бути ім'я методу об'єкта, заданого за допомогою функції [xml\_set\_object()](function.xml-set-object.md)

Сигнатура оброблювача має бути:

```methodsynopsis
handler(    XMLParser $parser,    string $open_entity_names,    string|false $base,    string $system_id,    string|false $public_id): bool
```

`parser`

XML-парсер, що викликає оброблювач.

`open_entity_names`

Список розділених пробілами імен сутностей, які можуть брати участь у аналізі поточної сутності (включаючи поточну сутність).

`base`

Це основа для дозволу системного ідентифікатора (`system_id`) Зовнішньої сутності.

`system_id`

Системний ідентифікатор у вигляді, як він представлений в оголошенні сутності.

`public_id`

Загальнодоступний ідентифікатор у вигляді, як і представлений у оголошенні сутності, чи порожній рядок, якщо такого немає; пробіли в ідентифікаторі будуть нормалізовані відповідно до вимог специфікації XML.

Обработчик должен вернуть\*\*`true`\*\*якщо сутність була оброблена, інакше він повинен повернути **`false`**При возврате значения**`false`**, XML-парсер прекращает разбор, а функция[xml\_get\_error\_code()](function.xml-get-error-code.md) повертає константу **`XML_ERROR_EXTERNAL_ENTITY_HANDLING`**

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |
| 7.3.0 | Возвращаемое значение`handler` більше не ігнорується, якщо модуль був зібраний із бібліотекою libxml. Раніше значення, що поверталося, ігнорувалося, а розбір ніколи не зупинявся. |
